# Com.covisint.messaging.custom.MessageAttributeSet
## When to use Service?
This service will take the service parameters from the rule configuration and set them as message attributes.  Please note that if you pick fields for the first time Connect doesn't know about, they will show up as blanks with the value in the message detail screen.   If you use an existing value already in the flow, this value will NOT be updated since it is only persisted during Phase 1.
## Service Description – Required

### Format:

FIELD1=XX,FIELD2=XX,ServiceType=MPI_PIX_QV3

In the service parms field, enter a list of values separated by a comma that need to be persisted in the message attribute area of tracker.

### Valid values:
Attributes
