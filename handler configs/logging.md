The logging handler defines how the event process should handle logging of events of this type.

```yaml
contextHandlers:
	# User defined handlerId, unique to this document and specific to this handler, along with operational control as to this handlers current operation
	- handlerId: 11111
		handlerStatus: enabled
		logging:
			loglevel: info
			retentionPeriod: 90
			# retention period in days for this log activity
```

