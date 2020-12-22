### M2 - Machine to Machine Event Context

The Machine to Machine Event Context or M2 for short, provides a specification to enable event processors (EP), asynchrouous APIs, Microservices and other interested parties, referred to as EP generically in this document, the ability to apply context in its processing to particluar event type. For example what should I do as an EP for logging, caching, failures etc for this event type.

A single EP may by design process many different event types with an M2 document created for each different event type or an M2 document may be applied to all events that are processed by an EP, via the use of wild carding. 

An M2 document can be applied by either a single named EP, via its name or name and group or a set of EPs grouped together that required common handling for events.

# Why M2

Historically with event driven architectures no common language has existed for expressing how an EP should handle an event, leaving this knowledge to be captured in plain text documentation or based on a developers understanding at that point in time. M2 enables events at scale, across countless event processors to have context applied in a consistent way.

Further details on [M2 Mec](https://m2mec.com)
