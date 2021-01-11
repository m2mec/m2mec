The ordering handler defines the order in which events should be processed

```yaml
contextHandlers:
 # User defined handlerId, unique to this document and specific to this handler, along with operational control as to this handlers current operation
  - handlerId: 777
    handlerStatus: enabled
    ordering:
     orderType: grouped
     # Order type, None, FIFO, LIFO or grouped
     groupBy: group_ident
     # The identifier to use for grouping
     
```

