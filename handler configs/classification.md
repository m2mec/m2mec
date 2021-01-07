How this event should be classified from a security or data protection point of view.

```yaml
contextHandlers:
	# User defined handlerId, unique to this document and specific to this handler, along with operational control as to this handlers current operation
	- handlerId: 222
		handlerStatus: enabled
		classification:
			classified: public
			# Supported classifications include public, internal, confidential and restricted. This should be used to inform on the handling of the event, from no specific security requirements as the data is widely available to specific handling required.
```

 