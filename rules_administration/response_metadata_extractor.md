# com.covisint.messaging.custom.metadataextract.extractor.ResponseMetadataExtractor
## When to use Service?
This Metadata Extractor is used to extract the response message codes of StatusCode and SubStatusCode and some additional attributes in Data tag, and then persist them as message attributes. The information is stored in a serialized com.covisint.tif.entity.common.ResponseStatus object that will need to be interrupt. This service will never fail for any reason. So if the object is corrupt, doesn't have the attribute, or missing payload, it will not fail. It's only available in Connect Onstar branch. To use the extractor, you have to set the following parameter - 'MetadataExtractor=ResponseMetadataExtractor'.

## Service Description – Required
### Format:
MetadataExtractor=ResponseMetadataExtractor,${attribute_name_1}=${attribute_value_1},${attribute_name_2}=${attribute_value_2},...

### Sample Configuration:
MetadataExtractor=ResponseMetadataExtractor,AccountNo=account_no

## Sample Input:

<?xml version="1.0" encoding="UTF-8" standalone="yes"?>< ns2:Response xmlns:ns2="http://www.covisint.com/tif/2010/response" xmlns="http://www.covisint.com/tif/2008/data">
<StatusCode xsi:type="xs:int" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xs="http://www.w3.org/2001/XMLSchema">200</StatusCode>
   <Data>
       <Attribute Name="account_no">
           <AttributeValue xsi:type="xs:string" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xs="http://www.w3.org/2001/XMLSchema">126261791</AttributeValue>
       </Attribute>
       <Attribute Name="app_session_key">
           <AttributeValue xsi:type="xs:string" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xs="http://www.w3.org/2001/XMLSchema">U9BOQ4R80ZB2NKSFQGZXNDUHSG2IFC0WGHVJLGHNYAXLTTDMLBYQG9SRZ</AttributeValue>
       </Attribute>
       <Attribute Name="country_id">
           <AttributeValue xsi:type="xs:string" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xs="http://www.w3.org/2001/XMLSchema">US</AttributeValue>
       </Attribute>
   </Data>
</ns2:Response>

## Sample Output
MESSAGE:ATTRIBUTES

Attribute Name: 	    Attribute Value

Status:          	    200

Account No: 	            126261791


## Errors

123 - Error occurs when extracting attributes from message payload.
