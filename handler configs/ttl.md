The Time To Live (TTL) handler defines how long events are valid, so ensuring that only relevant events are processed.

```yaml
contextHandlers:
 # User defined handlerId, unique to this document and specific to this handler, along with operational control as to this handlers current operation
  - handlerId: 444
    handlerStatus: enabled
    ttl:
     validFor: 43200
     #Number of seconds for event TTL
     
```

