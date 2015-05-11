# com.covisint.messaging.custom.metadataextract.xml.XpathMetadataExtractor

## When to use Service?

This Metadata Extractor is used to extract the XML node values based upon the given XPath and persist them as message attributes.

### Format:
'useXpath=yes'.

### Sample Configuration:

useXpath=yes,saveControlNo=yes,controlNumber=/DELFOR01/IDOC/EDI_DC40/DOCNUM
