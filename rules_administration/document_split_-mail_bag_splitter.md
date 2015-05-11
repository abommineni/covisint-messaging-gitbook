# Com.covisint.messaging.documentsplit.MailBagSplitter
## When to use Service?
This splitter can be used for splitting the mailbag documents that contain mixed data (X12, EDIFACT, XML, ICS, etc…).  If it is X12 data that the splitter is processing, it will handle data that contains many ISA’s, or one ISA with different ST’s.

## Splitter Data:

The following text can be used as the default “Splitter Data” on the splitting rule configuration for regular expression matching on the MailBagSplitter:

    (ISA[\'\*\:\!\"\&\(\)\+\,\-\.\/\;\?\=\%\~\@\[\]\_\{\}\\\|\<\>][ 0-9A-Z][ 0-9A-Z].)|(ICS..AIAG)|(UNA......UN[A-B].UNO[A-C].|UN[A-B].UNO[A-C].)|(<\\?xml)


This provides the splitter with a list of characters to search for to split documents.


For X12 data, the splitter will search for the value “ISA” and one of the characters in the text that follows.  If the data that you need to split contains a value that is not part of this list, you can add it in the format x’HexValue’.  For example, if the character following the ISA in the data you wish to split is a hex 15, configure the splitter data as follows:

    (ISA[\x'15'\'\*\:\!\"\&\(\)\+\,\-\.\/\;\?\=\%\~\@\[\]\_\{\}\\\|\<\>][ 0-9A-Z][ 0-9A-Z].)|(ICS..AIAG)|(UNA......UN[A-B].UNO[A-C].|UN[A-B].UNO[A-C].)|(<\\?xml)


Note: Future functionality of Connect will require the use of the MailbagSplitter to handle all EDI data.  Code will be added to the mailbag splitter to automatically call any additional splitters, such as the X12FirstTransSplitter or X12TwoPhaseSplitter, if needed.
