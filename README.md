# EdiEngine
Simple .NET EDI Reader, Writer and Validator.
Read, write and validate X12 EDI files with a parser written in C#.

## Main Features
* **EDI to JSON and JSON to EDI conversion**. 
EdiEngine uses Newtonsoft JSON for serialization, and raw Newtonsoft JSON reader for Deserialization. JSON is a handy extension for the library. Imagine you can parse your EDI object directly in an Angular or JQuery-based app.
* **EDI to XML and XML to EDI conversion**. EdiEngine does not use XML as an intermediary format, as many other engines do. It uses POCO objects and XML is just an extension.
* **Configurable EDI X12 997 - Functional Acknowledgment** generation. You can setup whether to accept all messages, accept but say errors were noted or reject depending on your needs.
* **HL Loop Hierarchical parsing** - Create a real tree structure based on HL segment hierarchy. No need to map every HL to map, this means one map can serve multiple needs. Say for ASN it can be S-O-P-I or S-O-I hierarchy in one map.
* **Syntax Notes**. All types of [EDI Syntax notes](https://github.com/olmelabs/EdiEngine/wiki/Syntax-Notes) are supported. P Paired, R Required, E Exclusion, C Conditional, L List Conditional
* **Composite Data Elements** are supported, which is really important for HIPAA and sometimes for other transactions even in retail.
* **X12 Maps** Current repository contains all 004010 maps, including Purchase Order, Invoice, Shipment and many others. You can easily craft yours on their basis.
* **.NET Standard 2.0 and Source Linking**. From version 1.6 repository only contains .NET Standard 2.0 projects. Source linking enabled, and symbol package is published to nuget symbols server, making debugging easier. Use version 1.5.2 for projects targeting .NET 4.5 (no source link or symbols available). 

## Installation
Clone the repository or install the Nuget package:

```
Install-Package xEdi.EdiEngine
```

## Documentation
Please use [Wiki](https://github.com/olmelabs/EdiEngine/wiki) for documentation and usage examples.

## Examples

Complete usage examples can be found in the test project.
