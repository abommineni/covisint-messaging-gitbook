# Com.covisint.messaging.custom.metadataextract.MetadataExtractionProcessor
## When to use Service?
This custom service will extract the attributes from message payload and apply them to the message attributes table, the service can also persist a attribute value to the control number field on message tracker when you set 'saveControlNo=yes' and specify a control number value by set parameter - 'controlNumber'.
## Service Description – Required

### Format:

 	useXpath=yes or no
 	saveControlNo=yes or no (TIP: The controlNumber value must be set when you want to save the value to the control number field on message tracker)
 	controlNumber=${ControlNumber_Path}
 	${attribute_key}=${attribue_value}
 	MetadataExtractor=RESTMetadataExtractor
