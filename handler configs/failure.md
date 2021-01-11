The failure handler defines how to handle any failures when processing events

```yaml
contextHandlers:
 # User defined handlerId, unique to this document and specific to this handler, along with operational control as to this handlers current operation
  - handlerId: 666
    handlerStatus: enabled
    failure:
     retryInterval: 180
     # Number of seconds between retry events for potential transient errors
     retryAttempts: 3
     # Number of retry events
     retryExhausted: drop
     # what to do when can no longer retry (DLQ = move event to Dead Letter Queue, Drop = drop event and continue processing, Halt = Halt all processing for this event type, i.e. don't process the next event)
     
```

