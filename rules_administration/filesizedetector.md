# Com.covisint.messaging.custom.FileSizeDetector
## When to use Service?
This custom service can be used for detecting the length of payload. If the length is larger than the number specified via the service params field, then the service will fail the message with the specified exception type ID.
## Service Description – Required

### Format:

FILE_SIZE=XXXX,TYPE_ID=XXXX
### Valid values:

 	FILE_SIZE: The param is used to set the maximum allowable byte size of the payload.
 	TYPE_ID: The param is used to set the exception type id that will bubble up to the dashboard if the file size of message exceeds the value set in the FILE_SIZE param

Errors :

6312 - Invalid service params for the custom service.
<TYPE_ID> - File size in this message is larger than the number set in service param 'FILE_SIZE'.
(Need to get TYPEID list)
