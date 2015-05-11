# Com.covisint.messaging.configurableSpliter.plugins.flatfile.PipeToNodeChildPlugin

## When to use Service?
PipeTONodeChildPlguin is a Pre-Messaging processing plugin that will take in a pipe delimited or csv delimited record and output an generic xml document

## Service Description – Not Required

### Sample Data

InputExample:



	ABC|DEF|G|HIJ|JKL|MNO|P
****ABC,DEF,G,HIJ,JKL,MNO,P
OutputExample:
ENV~~COVTEST~~COVTEST~1201:56, 29 July 2013 (EDT)~~
<?xml version="1.0" encoding="UTF-8"?>
<record>
    <field rrn="1">****ABC</field>
    <field rrn="2">DEF</field>
    <field rrn="3">G</field>
    <field rrn="4">HIJ</field>
    <field rrn="5">JKL</field>
    <field rrn="6">MNO</field>
    <field rrn="7">P
    </field>
</record>
ENV~~COVTEST~~COVTEST~1501:56, 29 July 2013 (EDT)~~
<?xml version="1.0" encoding="UTF-8"?>
<record>
    <field rrn="1">****ABC</field>
    <field rrn="2">DEF</field>
    <field rrn="3">G</field>
    <field rrn="4">HIJ</field>
    <field rrn="5">JKL</field>
    <field rrn="6">MNO</field>
    <field rrn="7">P
    </field>
</record>
