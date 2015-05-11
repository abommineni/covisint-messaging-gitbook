# EDI Data Streamer
##	813,'c','CustomProcessor.EDIDataStreamer:removeCharsBlock'
This service replaces 0D and 0A from the data stream with 1C and 1D and adds CRLF at the end of blocked data.
## 814,'c','CustomProcessor.EDIDataStreamer:removeExtraChars'
This service removes 0D and 0A from the data stream and it strips off EDS ELITE (TTR, THD, and TDS) headers and trailers.
## 844,'c','CustomProcessor.EDIDataStreamer:blockedDataWithLF'
This service replaces 0D and 0A from the data stream with 1C and 1D and adds LF at the end of blocked data.
