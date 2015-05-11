# 878,'c','com.covisint.messaging.custom.IDMEncoderDecoderService'

## When to use Service?
This custom service is used to encode/decode a service string/URL. User is required to enter if the service is used for encode or decode the incoming payload/URL. Also give details of what part of the payload (message) will be decoded/encoded. In below example, “ENCODE:REQUESTHEADERS” is  given as service parameter. All ‘’REQUESTHEADERS’’ in the payload will be encoded by the custom service.

## Service Description – Required

### Format:
matchString:comma separated parameters to encode /decode
EX: ENCODE:REQUESTHEADERS

### Valid values:

matchString  		  ENCODE, DECODE
parameters             	  REQUESTHEADERS, REQUESTPARAMETERS

### Limitations/rules:

1.	 Parameters to be encoded/decoded must be comma separated.
Ex: ENCODE: REQUESTHEADERS, REQUESTPARAMETERS
2.	 Single parameter
Ex: ENCODE: REQUESTHEADERS
3.	 If there is no parameter, by default REQUESTPARAMETERS is set as the parameter to be encoded/decoded.
Ex: DECODE

### Sample sender data and custom services modified output data:

Service description:

“ENCODE:REQUESTHEADERS”

Sample sender data:

SERVICENAME|SERVICENAME|Users
REQUESTHEADERS|cookie|WT_FPC=id=12.107.188.5-2029687696.30236349%3A%3A5CC05:lv=1354755483572:ss=1354755483572; __utma=18093099.1833825357.1342447811.1349288799.1358273887.6; __utmz=18093099.1342447811.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none)
REQUESTHEADERS|host|64.37.210.85:9080
REQUESTHEADERS|charset|UTF-8
REQUESTHEADERS|user-agent|Mozilla/5.0 (Windows NT 6.1; WOW64; rv:10.0.12) Gecko/20100101 Firefox/10.0.12
REQUESTHEADERS|client_id|e601da38c3ed20c97f1696cd0e2b561c
REQUESTHEADERS|accept-encoding|gzip
REQUESTHEADERS|accept-encoding|deflate
REQUESTHEADERS|Accept|text/html
REQUESTHEADERS|Accept|application/xhtml+xml
REQUESTHEADERS|Accept|application/xml;q=0.9
REQUESTHEADERS|Accept|*/*;q=0.8
REQUESTHEADERS|access_token|ZFMwdzBCeUhxcHNTREhWdVU4VE1iQXFVSXFCdXBjUm9tRlVIQlphQVVoM1dlc2Y1a25ieG1OTE01SEpVRVR4L1F3c0RRdXRMTmQvdTJJa0VUUTJxM21DSzFiUkhzT2IrTTBFTEhYbUVudzhJMkNITnVsUXhmamUweHhGbTV3MDFkWXFaVFZuZFYrZExGdFlkQTQ0YWcwRmh3cXYyZkQzMFY4TUl2WEtFN0RpMzE5L3Vlb2piMDAvVzA1clgvL1o2clQ4QXBIRUdOZnlTM1UzWHhOWjV5ZERmTjBzY21mS25xVTJCTk1RYnBHbWNFZDhTZ05TVmNGN0c3YUkrV3ZCNDRBZlp1bXdoM0hqTXhvTGZVRjJiQ1JHOElQVy9iRFR4T1AvOGd3amtHRmM9
REQUESTHEADERS|apikey|e601da38c3ed20c97f1696cd0e2b561c
REQUESTHEADERS|remote_address|64.37.204.110
REQUESTHEADERS|http_method|GET
REQUESTHEADERS|remote_host|64.37.204.110
REQUESTPARAMETERS|nonce|123
REQUESTPARAMETERS|timestamp|1358355879
REQUESTPARAMETERS|emailAddress|tkramer%40cov

Sample output for the above scenario:
SERVICENAME|SERVICENAME|Users
REQUESTHEADERS|cookie|WT_FPC%3Did%3D12.107.188.5-2029687696.30236349%253A%253A5CC05%3Alv%3D1354755483572%3Ass%3D1354755483572%3B+__utma%3D18093099.1833825357.1342447811.1349288799.1358273887.6%3B+__utmz%3D18093099.1342447811.1.1.utmcsr%3D%28direct%29|utmccn%3D%28direct%29|utmcmd%3D%28none%29
REQUESTHEADERS|host|64.37.210.85%3A9080
REQUESTHEADERS|charset|UTF-8
REQUESTHEADERS|user-agent|Mozilla%2F5.0+%28Windows+NT+6.1%3B+WOW64%3B+rv%3A10.0.12%29+Gecko%2F20100101+Firefox%2F10.0.12
REQUESTHEADERS|client_id|e601da38c3ed20c97f1696cd0e2b561c
REQUESTHEADERS|accept-encoding|gzip
REQUESTHEADERS|accept-encoding|deflate
REQUESTHEADERS|Accept|text%2Fhtml
REQUESTHEADERS|Accept|application%2Fxhtml%2Bxml
REQUESTHEADERS|Accept|application%2Fxml%3Bq%3D0.9
REQUESTHEADERS|Accept|*%2F*%3Bq%3D0.8
REQUESTHEADERS|access_token|ZFMwdzBCeUhxcHNTREhWdVU4VE1iQXFVSXFCdXBjUm9tRlVIQlphQVVoM1dlc2Y1a25ieG1OTE01SEpVRVR4L1F3c0RRdXRMTmQvdTJJa0VUUTJxM21DSzFiUkhzT2IrTTBFTEhYbUVudzhJMkNITnVsUXhmamUweHhGbTV3MDFkWXFaVFZuZFYrZExGdFlkQTQ0YWcwRmh3cXYyZkQzMFY4TUl2WEtFN0RpMzE5L3Vlb2piMDAvVzA1clgvL1o2clQ4QXBIRUdOZnlTM1UzWHhOWjV5ZERmTjBzY21mS25xVTJCTk1RYnBHbWNFZDhTZ05TVmNGN0c3YUkrV3ZCNDRBZlp1bXdoM0hqTXhvTGZVRjJiQ1JHOElQVy9iRFR4T1AvOGd3amtHRmM9
REQUESTHEADERS|apikey|e601da38c3ed20c97f1696cd0e2b561c
REQUESTHEADERS|remote_address|64.37.204.110
REQUESTHEADERS|http_method|GET
REQUESTHEADERS|remote_host|64.37.204.110
REQUESTPARAMETERS|nonce|123
REQUESTPARAMETERS|timestamp|1358355879
REQUESTPARAMETERS|emailAddress|tkramer%40cov

