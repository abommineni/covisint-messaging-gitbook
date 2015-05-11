# com.covisint.messaging.custom.metadataextract.extractor.RESTMetadataExtractor
## When to use Service?

This Metadata Extractor is used to capture REST service parms base upon the given parameters and persist them as message attributes.
## Service Description – Required
### Format:
- 'MetadataExtractor=RESTMetadataExtractor'.

Service Parameters
MetadataExtractor=RESTMetadataExtractor,${Attribute_Name}=${REQUESTHEADERS or REQUESTPARAMETERS pipe param name},...

### Sample Configuration:

MetadataExtractor=RESTMetadataExtractor,DeviceId=REQUESTPARAMETERS|device_id

### Sample Input:

SERVICENAME|SERVICENAME|UsernameToken('Saml20Token')
REQUESTHEADERS|cookie|_mkto_trk=id:721-YMN-235&token:_mch-covisint.com-1367592184082-27139
REQUESTHEADERS|content-type|application/x-www-form-urlencoded
REQUESTHEADERS|connection|keep-alive
REQUESTHEADERS|accept-language|en-us
REQUESTHEADERS|host|sts.qa.onstar.covisint.com
REQUESTHEADERS|content-length|128
REQUESTHEADERS|user-agent|CocoaRestClient/10 CFNetwork/596.4.3 Darwin/12.4.0 (x86_64) (MacBookPro6%2C2)
REQUESTHEADERS|accept-encoding|gzip
REQUESTHEADERS|accept-encoding|deflate
REQUESTHEADERS|Content-Type|application/x-www-form-urlencoded
REQUESTHEADERS|proxy-connection|keep-alive
REQUESTHEADERS|Accept|/
REQUESTHEADERS|connect_guid|130628093314619-331-22521-EXLAQ664-IW7C0S
REQUESTHEADERS|http_method|POST
REQUESTHEADERS|remote_address|12.107.188.5
REQUESTHEADERS|remote_host|12.107.188.5
REQUESTPARAMETERS|partner_app_password|VoltWeb_123
REQUESTPARAMETERS|partner_app_id|VOLT_WEB_V1
REQUESTPARAMETERS|device_id|X1001
REQUESTPARAMETERS|password|test1234
REQUESTPARAMETERS|username|test84352
REQUESTPARAMETERS|format_type|xml

### Sample Output:
MESSAGE ATTRIBUTES
Attribute Name: 	Attribute Value:
Device Id 	X1001

