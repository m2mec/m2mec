The range of events (based on an event identifier) that should be processed by this event processor

```yaml
contextHandlers:
 # User defined handlerId, unique to this document and specific to this handler, along with operational control as to this handlers current operation
  - handlerId: 888
    handlerStatus: enabled
    range:
     processFrom: 20000
     # The event id to start processing from
     processTo: 30000
     # The event id to process up to, -1 would indicate no upper boundary
     
```

