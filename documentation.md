---
title: Documentation
nav_order: 2
---

# Installation

From Google Sheets, click on Extensions/... You then arrive to the Google Workspace Marketplace screen.

Type "Driven by sheets" in the search box: one or more extensions appear. Click on the Sheep :-)

A screen then presents you the extension, the scopes and the opinions. Read carefully the scopes you'll need to give to the extension so it can process your documents. More information is available [here](https://driven-by-sheets/public/scopes).

Click on Install to install.

# Sheet

The sheet is composed of 2 columns A and B:

* The column A contains the *name* of the data. For example: Firstname
* The column B contains the *data* itself. For example: John

The firstname is also often refered as the variable name.

A variable may be a parameter or a data:

* a parameter is used by the program itself. For example, a destination folder to store the generated documents, name of the models to be used by the program to know which templates to process. The program and each of its versions come with a set of predefined variables.
* a data is your information only and are not used by the program for its internal use.

## Parameters

A parameter is not directly used in templates but gives the program to process a certain way. The following parameters are available :

* destination path
* models

## Data

# Template

A template may contain, besides usual content, somme markers and some conditional sections.

## Markers

The markers, labels surrounded by "{{" and "}}", replaced by the values contained in the Sheet. If they are not defined, they remain untouched. For example, if my variable, named in the sheet FIRSTNAME, contains John in the cell, then the following will be replaced by John

{{FIRSTNAME}} => John

Of course, the text of the format is conserved.

## Conditional sections

A conditional section is enclosed by the a start and end tag like these ones :

[IF NAME == John]
Chief {{FIRSTNAME}}
[/IF]

[IF NAME != John]
{{FIRSTNAME}}
[/IF]

The start tag contains a condition, or set of conditions (for the moment related only by AND) with the use of the && operator. For example :

[IF FIRSTNAME == Jonh && NAME == Davis]
Chief {{FIRSTNAME}} {{NAME}}
[/IF]
