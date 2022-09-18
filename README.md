Track ETL Challenge 9 - Mermaid to Logic
================

# Issue
CfE researchers (note: non-technical staff with limited coding expertise) use Mermaid diagrams to define the operationalization of outcome variables (‘Diversitätsprofil’). For calculating these outcome variables, they use a seperate, hard-coded R script. We want to streamline this process! 

# Goal
Translation of information from Mermaid diagrams into YAML-style data structures. (note: Team 7 (ETL - Transform) already wrote a Python script to automatically calculate the outcome variables based on YAML-style data structures). No more separate, hard-coded R scripts. 

# Solutions 

1. Use a predefined Mermaid style guide to create the mermaid diagrams.

- template with defined blocks, indicated by tripe %, e.g. %%%domain
- define variables first, add paths afterwards, add visual boxes (with subgraph) later
- additional comments can be included using double %
- naming convention: name outcome variables with the official CfN labels, name input variables with the official survey label (caution: input variables have a changing prefix for each study domain (e.g. q1) + name (e.g. x1_SQ001) → q1x1_SQ001) 
- add desired descriptions (e.g. the verbatim question) in brackets after the label, e.g. migH["Kein Migrationshintergrund"

2. Write code in Python or R to transfer the Mermaid code to a YAML-style data structure.
