# com.covisint.messaging.custom.metadataextract.xml.SaxMetadataExtractor
## When to use Service?

This Metadata Extractor is used to extract the XML node values based upon the SAX parser and persist them as message attributes.
## Service Description – Required
### Format:
'useXpath=no', this is a default Metadata Extractor.

### Sample Configuration:

useXpath=no,saveControlNo=yes,controlNumber=${node_name},...


