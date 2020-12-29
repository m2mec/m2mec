### M2 - Machine to Machine Event Context

The Machine to Machine Event Context or M2 for short, provides a specification to enable event processors (EP), asynchrouous APIs, Microservices and other interested parties, referred to as EP generically in this document, the ability to apply context in its processing to particluar event type. For example what should I do as an EP for logging, caching, failures etc for this event type.

A single EP may by design process many different event types with an M2 document created for each different event type or an M2 document may be applied to all events that are processed by an EP, via the use of wild carding. 

An M2 document can be applied by either a single named EP, via its name or name and group or a set of EPs grouped together that required common handling for events.

### Why M2

Historically with event driven architectures no common language has existed for expressing how an EP should handle an event, leaving this knowledge to be captured in plain text documentation or based on a developers understanding at that point in time. M2 enables events at scale, across countless event processors to have context applied in a consistent way. Further details on [M2 Mec](https://m2mec.com)

### M2 Mec Specification

The M2 Mec Specification schema is structured as follows (this is based on the [COA example](https://github.com/m2mec/m2mec/blob/main/examples/v0.1/m2-example.yaml)),

```yaml
# identifier block - required
# m2mech: Version
m2mech: 0.0.1
# id: A unique identifier for specification, identified with reverse dns format
# Supports both public & private name sapces
id: coa-sample-doc.m2def.m2mec.com
# status: The status of the m2mech definition, enabled, disabled, drop
# Enabled - Use to Process, Disabled - Don't process events, Drop - Ack & drop
status: enabled
```

```yaml
# Information Block
info:
# Title of this definition
  title: Example M2 definition - This is the version for this processor/event
# Version of this definition
  version: 1.0.0
```

```yaml
# Event - The event that this definition applies to
event:
# Unique identifier
  eventTypeId: 12345
# Human friendly name for this event type
  eventName: changeOfAddress
```

```yaml
# The event processor (EP) or group of event processors this definition should be processed by
processors:
# processorIdentifier: Reverse DNS for this event processor
  processorIdentifier: sample-service.micro-service.com
# processorGroup: Group idenitifer to enable EP's with same processing requirements to leverage a single config
  processorGroup: testGroup
```

```yaml
# Contexthandlers: An array of handlers that the EP should apply to the event when being processed
contextHandlers:
# handlerId: User defined id unique for this definition file for this handler
  - handlerId: 111111
# handlerStatus: if this particular handler is enabled or disabled
    handlerStatus: enabled
# handler: Core handler name
    handler: logging
# Specific handler configuration
    logging:
      loglevel: info
      rententionPeriod: 60
```

```yaml
# extensions: An array of an extenstions that are defined in this document
extensions:
# extensionId: Unique id for this extension using reverse dns
  - extensionId: amazon-state-language.mytest.bigco.com
# extension specific config
    description: State control
    extension: "Note this would be the embedded state language definition"
```

