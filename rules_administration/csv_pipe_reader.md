# Com.covisint.messaging.configurableSpliter.reader.CSVPipeReader
## When to use Service?
CSVPipeReader is used to inspect and split the payload with CSV or Pipe format to multiple child payload.
## Service Description –  Required
### Format:
Record Identification1:Used to identify one of the major routing attributes.

Remove Header Record:Used to specify whether to reomve the head record in the child message.
###Input Example:

SiteName|SiteIdentifier|SiteIdentifierName|MedRecNo|CSV|PatientFirstName|PatientLastName|PatientIdentifier|PatientIdentifierName|Gender|Birthdate|ProviderUPIN|ProviderName|MeasureName|TransactValue|TransactLogic|TransactGoalMin|TransactGoalMax|TransactInterval|TransactDueDate|TransactDate|Comment|ExternalRecordNumber
    HMHMM|||013343082|CSV|GERALD|LEBLANC-FORD|0133430823350|ACCT NUM|M|09/21/1944||Provider name|Tobacco Use/Exposure Assessment|never smoker||||||12/16/2013||
HMHHH|||015144009|CSV|THERESA|DRAINE|0151440093350|ACCT NUM|F|08/20/1961||Provider name|Tobacco Use/Exposure Assessment|never smoker||||||12/16/2013||
HMHMM|||015560659|CSV|WILLIAM|LARUBBRO|0155606593350|ACCT NUM|M|05/11/1933||Provider name|Tobacco Use/Exposure Assessment|never smoker||||||12/17/2013||
HMHWB|||016908840|CSV|JOHN|GUNDRUM|0169088403351|ACCT NUM|M|02/14/1966||Provider name|Tobacco Use/Exposure Assessment|current every day smoker||||||12/17/2013||
HMHMM|||019830355|CSV|SUSAN|CARANTO|0198303553351|ACCT NUM|F|04/10/1950||Provider name|Tobacco Use/Exposure Assessment|never smoker||||||12/17/2013||

###Output Example:

Record Identification 1:5

Message Routing: Document Type:Record Identifier 1

Remove Header Record:checked

    ENV~~COVTEST~~COVTEST~24001:29, 25 February 2014 (EST)~~
HMHMM|||013343082|CSV|GERALD|LEBLANC-FORD|0133430823350|ACCTNUM|M|09/21/1944||PROVIDER NAME|TOBACCO USE/EXPOSURE               ASSESSMENT|NEVER SMOKER||||||12/16/2013||

    ENV~~COVTEST~~COVTEST~24101:29, 25 February 2014 (EST)~~
HMHHH|||015144009|CSV|THERESA|DRAINE|0151440093350|ACCT NUM|F|08/20/1961||PROVIDER NAME|TOBACCO USE/EXPOSURE ASSESSMENT|NEVER SMOKER||||||12/16/2013||

    ENV~~COVTEST~~COVTEST~24201:29, 25 February 2014 (EST)~~
HMHMM|||015560659|CSV|WILLIAM|LARUBBRO|0155606593350|ACCT NUM|M|05/11/1933||PROVIDER NAME|TOBACCO USE/EXPOSURE ASSESSMENT|NEVER SMOKER||||||12/17/2013||

    ENV~~COVTEST~~COVTEST~24301:29, 25 February 2014 (EST)~~
HMHWB|||016908840|CSV|JOHN|GUNDRUM|0169088403351|ACCT NUM|M|02/14/1966||PROVIDER NAME|TOBACCO USE/EXPOSURE ASSESSMENT|CURRENT EVERY DAY SMOKER||||||12/17/2013||

    ENV~~COVTEST~~COVTEST~24401:29, 25 February 2014 (EST)~~
HMHMM|||019830355|CSV|SUSAN|CARANTO|0198303553351|ACCT NUM|F|04/10/1950||PROVIDER NAME|TOBACCO USE/EXPOSURE ASSESSMENT|NEVER SMOKER||||||12/17/2013||
