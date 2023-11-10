---
title: "NCCS PACs Data Catalog"
format: html
editor: visual
execute: 
  echo: false
  warning: false
---

::: {.cell}

:::


<br>

<hr>

<br>

*Last updated May 2023*


## Organizational Data


<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-FM-8871.csv" class='button'> FORM 8871 </a>

<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-SCHED-D.csv" class='button'> SCHEDULE D </a>

<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-SCHED-E.csv" class='button'> SCHEDULE E </a>

<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-SCHED-R.csv" class='button'> SCHEDULE R </a>


## Activities Data

<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-FM-8872.csv" class='button'> FORM 8872 </a>

<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-SCHED-A.csv" class='button'> SCHEDULE A </a>

<a href="https://nccsdata.s3.us-east-1.amazonaws.com/public/pacs/2023-05-POL-ORGS-SCHED-B.csv" class='button'> SCHEDULE B </a>






# Data Dictionaries 

The [**data-dictionary.csv**](tidy-data-dictionary.csv) file is machine-readable version of [**PolOrgsFileLayout.doc**](https://github.com/Nonprofit-Open-Data-Collective/irs-527-political-action-committee-disclosures/raw/main/PolOrgsFileLayout.doc).

## TABLES 

Form 8871 Tables

* **D**: If Director and Officer records exist for an 8871 Form, each record will be printed out in a “D” record.  The “D” records for a given 8871 Form will follow it’s related “1” Record.  There may be several “D” records for any one “1” record. 
* **E**: If the PAC has provided an Election Authority Identification Number (EAIN) on the 8871 Form, each record will be printed out in an “E” record.  The “E” records for a given 8871 Form will follow its related “1” Record.  There may be several “E” records for any one “1” record. 
* **R**: If Related Entities records exist for an 8871 Form, each record will be printed out in a “R” record.  The “R” records for a given 8871 Form will follow it’s related “1” Record.  There may be several “R” records for any one “1” record. 

Form 8872 Tables

  
* **A**: If a Schedule A exists for an 8872 Form, each Schedule A record will be printed out in an “A” record.  The “A” records for a given 8872 Form will follow its related “2” Record.  There may be several “A” records for any one “2” record. 
* **B**: If a Schedule B exists for an 8872 Form, each Schedule B record will be printed out in an “B” record.  The “B” records for a given 8872 Form will follow its related “2” Record.  There may be several “B” records for any one “2” record. 



## FM-8871 


|IRS_FIELD_NAME             |SIZE            |VALID_VALUES          |FORMAT       |DESCRIPTION               |FORMTYPE | ORDER|F_ORDER    |VARNAME                    |
|:--------------------------|:---------------|:---------------------|:------------|:-------------------------|:--------|-----:|:----------|:--------------------------|
|Record Type                |1               |1                     |Numeric      |Designates an 8871 Record |FM-8871  |     1|FM-8871-01 |RECORD_TYPE                |
|Form Type                  |10              |8871                  |Numeric      |                          |FM-8871  |     3|FM-8871-03 |FORM_TYPE                  |
|Form ID Number             |Up to 38 digits |                      |Numeric      |                          |FM-8871  |     5|FM-8871-05 |FORM_ID_NUMBER             |
|Initial Report Indicator   |1               |1 or 0                |Numeric      |1 = Initial Report        |FM-8871  |     7|FM-8871-07 |INITIAL_REPORT_INDICATOR   |
|                           |                |                      |             |0 = Not Initial           |FM-8871  |     8|FM-8871-08 |                           |
|Amended Report Indicator   |1               |1 or 0                |Numeric      |1 = Amended               |FM-8871  |    10|FM-8871-10 |AMENDED_REPORT_INDICATOR   |
|                           |                |                      |             |0 = Not Amended           |FM-8871  |    11|FM-8871-11 |                           |
|Final Report Indicator     |1               |1 or 0                |Numeric      |1 = Final Report          |FM-8871  |    13|FM-8871-13 |FINAL_REPORT_INDICATOR     |
|                           |                |                      |             |0 = Not Final             |FM-8871  |    14|FM-8871-14 |                           |
|EIN                        |9               |                      |AlphaNumeric |                          |FM-8871  |    16|FM-8871-16 |EIN                        |
|ORGANIZATION NAME          |70              |                      |AlphaNumeric |                          |FM-8871  |    18|FM-8871-18 |ORGANIZATION_NAME          |
|MAILING ADDRESS 1          |50              |                      |AlphaNumeric |                          |FM-8871  |    20|FM-8871-20 |MAILING_ADDRESS_1          |
|MAILING ADDRESS 2          |50              |                      |AlphaNumeric |                          |FM-8871  |    22|FM-8871-22 |MAILING_ADDRESS_2          |
|MAILING ADDRESS CITY       |50              |                      |AlphaNumeric |                          |FM-8871  |    24|FM-8871-24 |MAILING_ADDRESS_CITY       |
|MAILING ADDRESS STATE      |2               |                      |AlphaNumeric |                          |FM-8871  |    26|FM-8871-26 |MAILING_ADDRESS_STATE      |
|MAILING ADDRESS ZIP CODE   |5               |                      |AlphaNumeric |                          |FM-8871  |    28|FM-8871-28 |MAILING_ADDRESS_ZIP_CODE   |
|MAILING ADDRESS ZIP EXT    |4               |                      |AlphaNumeric |                          |FM-8871  |    30|FM-8871-30 |MAILING_ADDRESS_ZIP_EXT    |
|E_MAIL ADDRESS             |150             |                      |AlphaNumeric |                          |FM-8871  |    32|FM-8871-32 |E_MAIL_ADDRESS             |
|ESTABLISHED DATE           |8               |                      |AlphaNumeric |                          |FM-8871  |    34|FM-8871-34 |ESTABLISHED_DATE           |
|CUSTODIAN NAME             |50              |                      |AlphaNumeric |                          |FM-8871  |    36|FM-8871-36 |CUSTODIAN_NAME             |
|CUSTODIAN ADDRESS 1        |50              |                      |AlphaNumeric |                          |FM-8871  |    38|FM-8871-38 |CUSTODIAN_ADDRESS_1        |
|CUSTODIAN ADDRESS 2        |50              |                      |AlphaNumeric |                          |FM-8871  |    40|FM-8871-40 |CUSTODIAN_ADDRESS_2        |
|CUSTODIAN ADDRESS CITY     |50              |                      |AlphaNumeric |                          |FM-8871  |    42|FM-8871-42 |CUSTODIAN_ADDRESS_CITY     |
|CUSTODIAN ADDRESS STATE    |2               |                      |AlphaNumeric |                          |FM-8871  |    44|FM-8871-44 |CUSTODIAN_ADDRESS_STATE    |
|CUSTODIAN ADDRESS ZIP CODE |5               |                      |AlphaNumeric |                          |FM-8871  |    46|FM-8871-46 |CUSTODIAN_ADDRESS_ZIP_CODE |
|CUSTODIAN ADDRESS ZIP EXT  |4               |                      |AlphaNumeric |                          |FM-8871  |    48|FM-8871-48 |CUSTODIAN_ADDRESS_ZIP_EXT  |
|CONTACT PERSON NAME        |50              |                      |AlphaNumeric |                          |FM-8871  |    50|FM-8871-50 |CONTACT_PERSON_NAME        |
|CONTACT ADDRESS 1          |50              |                      |AlphaNumeric |                          |FM-8871  |    52|FM-8871-52 |CONTACT_ADDRESS_1          |
|CONTACT ADDRESS 2          |50              |                      |AlphaNumeric |                          |FM-8871  |    54|FM-8871-54 |CONTACT_ADDRESS_2          |
|CONTACT ADDRESS CITY       |50              |                      |AlphaNumeric |                          |FM-8871  |    56|FM-8871-56 |CONTACT_ADDRESS_CITY       |
|CONTACT ADDRESS STATE      |2               |                      |AlphaNumeric |                          |FM-8871  |    58|FM-8871-58 |CONTACT_ADDRESS_STATE      |
|CONTACT ADDRESS ZIP CODE   |5               |                      |AlphaNumeric |                          |FM-8871  |    60|FM-8871-60 |CONTACT_ADDRESS_ZIP_CODE   |
|CONTACT ADDRESS ZIP EXT    |4               |                      |AlphaNumeric |                          |FM-8871  |    62|FM-8871-62 |CONTACT_ADDRESS_ZIP_EXT    |
|BUSINESS ADDRESS 1         |50              |                      |AlphaNumeric |                          |FM-8871  |    64|FM-8871-64 |BUSINESS_ADDRESS_1         |
|BUSINESS ADDRESS 2         |50              |                      |AlphaNumeric |                          |FM-8871  |    66|FM-8871-66 |BUSINESS_ADDRESS_2         |
|                           |                |                      |             |                          |FM-8871  |    68|FM-8871-68 |                           |
|BUSINESS ADDRESS CITY      |50              |                      |AlphaNumeric |                          |FM-8871  |    69|FM-8871-69 |BUSINESS_ADDRESS_CITY      |
|BUSINESS ADDRESS STATE     |2               |                      |AlphaNumeric |                          |FM-8871  |    71|FM-8871-71 |BUSINESS_ADDRESS_STATE     |
|BUSINESS ADDRESS ZIP CODE  |5               |                      |AlphaNumeric |                          |FM-8871  |    73|FM-8871-73 |BUSINESS_ADDRESS_ZIP_CODE  |
|BUSINESS ADDRESS ZIP EXT   |4               |                      |AlphaNumeric |                          |FM-8871  |    75|FM-8871-75 |BUSINESS_ADDRESS_ZIP_EXT   |
|EXEMPT 8872 INDICATOR      |1               |1 or 0                |AlphaNumeric |                          |FM-8871  |    77|FM-8871-77 |EXEMPT_8872_INDICATOR      |
|EXEMPT STATE               |2               |                      |AlphaNumeric |                          |FM-8871  |    79|FM-8871-79 |EXEMPT_STATE               |
|EXEMPT 990 INDICATOR       |1               |1 or 0                |AlphaNumeric |                          |FM-8871  |    81|FM-8871-81 |EXEMPT_990_INDICATOR       |
|PURPOSE                    |512             |                      |AlphaNumeric |                          |FM-8871  |    83|FM-8871-83 |PURPOSE                    |
|MATERIAL CHANGE DATE       |8               |                      |AlphaNumeric |                          |FM-8871  |    85|FM-8871-85 |MATERIAL_CHANGE_DATE       |
|INSERT_DATETIME            |19              |YYYY-MM-DD HH24:MI:SS |Datetime     |                          |FM-8871  |    87|FM-8871-87 |INSERT_DATETIME            |
|RELATED_ENTITY_BYPASS      |1               |1 or 0                |AlphaNumeric |0 = Entities Exist        |FM-8871  |    89|FM-8871-89 |RELATED_ENTITY_BYPASS      |
|                           |                |                      |             |1 = No Entities           |FM-8871  |    90|FM-8871-90 |                           |
|EAIN_BYPASS                |1               |1 or 0                |AlphaNumeric |0 = EAIN(s) Exist         |FM-8871  |    92|FM-8871-92 |EAIN_BYPASS                |
|                           |                |                      |             |1 = No EAINS              |FM-8871  |    93|FM-8871-93 |                           |



### SCHED-D


|IRS_FIELD_NAME              |SIZE            |VALID_VALUES |FORMAT       |DESCRIPTION                                                  |FORMTYPE | ORDER|F_ORDER    |VARNAME                     |
|:---------------------------|:---------------|:------------|:------------|:------------------------------------------------------------|:--------|-----:|:----------|:---------------------------|
|Record Type                 |1               |D            |Alphanumeric |Designates a Director/Officer Record for an 8871 Form Record |SCHED-D  |     1|SCHED-D-01 |RECORD_TYPE                 |
|Form ID Number              |Up to 38 digits |             |Numeric      |                                                             |SCHED-D  |     3|SCHED-D-03 |FORM_ID_NUMBER              |
|DIRECTOR ID                 |Up to 38 digits |             |Numeric      |                                                             |SCHED-D  |     5|SCHED-D-05 |DIRECTOR_ID                 |
|ORG NAME                    |70              |             |AlphaNumeric |                                                             |SCHED-D  |     7|SCHED-D-07 |ORG_NAME                    |
|EIN                         |9               |             |AlphaNumeric |                                                             |SCHED-D  |     9|SCHED-D-09 |EIN                         |
|ENTITY NAME                 |50              |             |AlphaNumeric |                                                             |SCHED-D  |    11|SCHED-D-11 |ENTITY_NAME                 |
|ENTITY TITLE                |50              |             |AlphaNumeric |                                                             |SCHED-D  |    13|SCHED-D-13 |ENTITY_TITLE                |
|ENTITY ADDRESS 1            |50              |             |AlphaNumeric |                                                             |SCHED-D  |    15|SCHED-D-15 |ENTITY_ADDRESS_1            |
|ENTITY ADDRESS 2            |50              |             |AlphaNumeric |                                                             |SCHED-D  |    17|SCHED-D-17 |ENTITY_ADDRESS_2            |
|ENTITY ADDRESS CITY         |50              |             |AlphaNumeric |                                                             |SCHED-D  |    19|SCHED-D-19 |ENTITY_ADDRESS_CITY         |
|ENTITY ADDRESS ST           |2               |             |AlphaNumeric |                                                             |SCHED-D  |    21|SCHED-D-21 |ENTITY_ADDRESS_ST           |
|ENTITY ADDRESS ZIP CODE     |5               |             |AlphaNumeric |                                                             |SCHED-D  |    23|SCHED-D-23 |ENTITY_ADDRESS_ZIP_CODE     |
|ENTITY ADDRESS ZIP CODE EXT |4               |             |AlphaNumeric |                                                             |SCHED-D  |    25|SCHED-D-25 |ENTITY_ADDRESS_ZIP_CODE_EXT |



### SCHED-E


|IRS_FIELD_NAME               |SIZE            |VALID_VALUES                                                                             |FORMAT       |DESCRIPTION                                |FORMTYPE | ORDER|F_ORDER    |VARNAME                      |
|:----------------------------|:---------------|:----------------------------------------------------------------------------------------|:------------|:------------------------------------------|:--------|-----:|:----------|:----------------------------|
|Record Type                  |1               |E                                                                                        |Alphanumeric |Designates an EAIN Record for an 8871 form |SCHED-E  |     1|SCHED-E-01 |RECORD_TYPE                  |
|Form ID Number               |Up to 38 digits |                                                                                         |Numeric      |                                           |SCHED-E  |     3|SCHED-E-03 |FORM_ID_NUMBER               |
|EAIN ID                      |Up to 38 digits |                                                                                         |Numeric      |                                           |SCHED-E  |     5|SCHED-E-05 |EAIN_ID                      |
|ELECTION AUTHORITY ID NUMBER |30              |                                                                                         |AlphaNumeric |                                           |SCHED-E  |     7|SCHED-E-07 |ELECTION_AUTHORITY_ID_NUMBER |
|STATE_ISSUED                 |2               |2 letter abbreviations of all 50 states or FD for Federal or DC for District of Columbia |AlphaNumeric |                                           |SCHED-E  |     9|SCHED-E-09 |STATE_ISSUED                 |



### SCHED-R


|IRS_FIELD_NAME          |SIZE            |VALID_VALUES |FORMAT       |DESCRIPTION                                         |FORMTYPE | ORDER|F_ORDER    |VARNAME                 |
|:-----------------------|:---------------|:------------|:------------|:---------------------------------------------------|:--------|-----:|:----------|:-----------------------|
|Record Type             |1               |R            |Alphanumeric |Designates a Related Entity Record for an 8871 Form |SCHED-R  |     1|SCHED-R-01 |RECORD_TYPE             |
|Form ID Number          |Up to 38 digits |             |Numeric      |                                                    |SCHED-R  |     3|SCHED-R-03 |FORM_ID_NUMBER          |
|ENTITY ID               |Up to 38 digits |             |Numeric      |                                                    |SCHED-R  |     5|SCHED-R-05 |ENTITY_ID               |
|ORG NAME                |70              |             |AlphaNumeric |                                                    |SCHED-R  |     7|SCHED-R-07 |ORG_NAME                |
|EIN                     |9               |             |AlphaNumeric |                                                    |SCHED-R  |     9|SCHED-R-09 |EIN                     |
|ENTITY NAME             |50              |             |AlphaNumeric |                                                    |SCHED-R  |    11|SCHED-R-11 |ENTITY_NAME             |
|ENTITY RELATIONSHIP     |50              |             |AlphaNumeric |                                                    |SCHED-R  |    13|SCHED-R-13 |ENTITY_RELATIONSHIP     |
|ENTITY ADDRESS 1        |50              |             |AlphaNumeric |                                                    |SCHED-R  |    15|SCHED-R-15 |ENTITY_ADDRESS_1        |
|ENTITY ADDRESS 2        |50              |             |AlphaNumeric |                                                    |SCHED-R  |    17|SCHED-R-17 |ENTITY_ADDRESS_2        |
|ENTITY ADDRESS CITY     |50              |             |AlphaNumeric |                                                    |SCHED-R  |    19|SCHED-R-19 |ENTITY_ADDRESS_CITY     |
|ENTITY ADDRESS ST       |2               |             |AlphaNumeric |                                                    |SCHED-R  |    21|SCHED-R-21 |ENTITY_ADDRESS_ST       |
|ENTITY ADDRESS ZIP CODE |5               |             |AlphaNumeric |                                                    |SCHED-R  |    23|SCHED-R-23 |ENTITY_ADDRESS_ZIP_CODE |
|ENTITY ADDRESS ZIP EXT  |4               |             |AlphaNumeric |                                                    |SCHED-R  |    25|SCHED-R-25 |ENTITY_ADDRESS_ZIP_EXT  |




## FM-8872


|IRS_FIELD_NAME              |SIZE            |VALID_VALUES                |FORMAT       |DESCRIPTION                                 |FORMTYPE | ORDER|F_ORDER    |VARNAME                     |
|:---------------------------|:---------------|:---------------------------|:------------|:-------------------------------------------|:--------|-----:|:----------|:---------------------------|
|Record Type                 |1               |2                           |Alphanumeric |Designates an 8872 Form Record              |FM-8872  |     1|FM-8872-01 |RECORD_TYPE                 |
|Form Type                   |10              |8872                        |Numeric      |                                            |FM-8872  |     3|FM-8872-03 |FORM_TYPE                   |
|Form ID Number              |Up to 38 digits |                            |Numeric      |                                            |FM-8872  |     5|FM-8872-05 |FORM_ID_NUMBER              |
|PERIOD Begin Date           |8               |                            |AlphaNumeric |                                            |FM-8872  |     7|FM-8872-07 |PERIOD_BEGIN_DATE           |
|PERIOD End Date             |8               |                            |AlphaNumeric |                                            |FM-8872  |     9|FM-8872-09 |PERIOD_END_DATE             |
|Initial Report Indicator    |1               |1 or 0                      |Numeric      |1 = Initial Report                          |FM-8872  |    11|FM-8872-11 |INITIAL_REPORT_INDICATOR    |
|                            |                |                            |             |0 = Not Initial                             |FM-8872  |    12|FM-8872-12 |                            |
|Amended Report Indicator    |1               |1 or 0                      |Numeric      |1 = Amended                                 |FM-8872  |    14|FM-8872-14 |AMENDED_REPORT_INDICATOR    |
|                            |                |                            |             |0 = Not Amended                             |FM-8872  |    15|FM-8872-15 |                            |
|Final Report Indicator      |1               |1 or 0                      |Numeric      |1 = Final Report                            |FM-8872  |    17|FM-8872-17 |FINAL_REPORT_INDICATOR      |
|                            |                |                            |             |0 = Not Final                               |FM-8872  |    18|FM-8872-18 |                            |
|Change of Address Indicator |1               |1 or 0                      |Numeric      |1 = Address has changed                     |FM-8872  |    20|FM-8872-20 |CHANGE_OF_ADDRESS_INDICATOR |
|                            |                |                            |             |0 = Address has not changed                 |FM-8872  |    21|FM-8872-21 |                            |
|ORGANIZATION NAME           |70              |                            |AlphaNumeric |                                            |FM-8872  |    23|FM-8872-23 |ORGANIZATION_NAME           |
|EIN                         |9               |                            |AlphaNumeric |                                            |FM-8872  |    25|FM-8872-25 |EIN                         |
|MAILING ADDRESS 1           |50              |                            |AlphaNumeric |                                            |FM-8872  |    27|FM-8872-27 |MAILING_ADDRESS_1           |
|MAILING ADDRESS 2           |50              |                            |AlphaNumeric |                                            |FM-8872  |    29|FM-8872-29 |MAILING_ADDRESS_2           |
|MAILING ADDRESS CITY        |50              |                            |AlphaNumeric |                                            |FM-8872  |    31|FM-8872-31 |MAILING_ADDRESS_CITY        |
|MAILING ADDRESS STATE       |2               |                            |AlphaNumeric |                                            |FM-8872  |    33|FM-8872-33 |MAILING_ADDRESS_STATE       |
|MAILING ADDRESS ZIP CODE    |5               |                            |AlphaNumeric |                                            |FM-8872  |    35|FM-8872-35 |MAILING_ADDRESS_ZIP_CODE    |
|MAILING ADDRESS ZIP EXT     |4               |                            |AlphaNumeric |                                            |FM-8872  |    37|FM-8872-37 |MAILING_ADDRESS_ZIP_EXT     |
|E_MAIL ADDRESS              |150             |                            |AlphaNumeric |                                            |FM-8872  |    39|FM-8872-39 |E_MAIL_ADDRESS              |
|ORG FORMATION DATE          |8               |                            |AlphaNumeric |                                            |FM-8872  |    41|FM-8872-41 |ORG_FORMATION_DATE          |
|CUSTODIAN NAME              |50              |                            |AlphaNumeric |                                            |FM-8872  |    43|FM-8872-43 |CUSTODIAN_NAME              |
|CUSTODIAN ADDRESS 1         |50              |                            |AlphaNumeric |                                            |FM-8872  |    45|FM-8872-45 |CUSTODIAN_ADDRESS_1         |
|CUSTODIAN ADDRESS 2         |50              |                            |AlphaNumeric |                                            |FM-8872  |    47|FM-8872-47 |CUSTODIAN_ADDRESS_2         |
|CUSTODIAN ADDRESS CITY      |50              |                            |AlphaNumeric |                                            |FM-8872  |    49|FM-8872-49 |CUSTODIAN_ADDRESS_CITY      |
|CUSTODIAN ADDRESS STATE     |2               |                            |AlphaNumeric |                                            |FM-8872  |    51|FM-8872-51 |CUSTODIAN_ADDRESS_STATE     |
|CUSTODIAN ADDRESS ZIP CODE  |5               |                            |AlphaNumeric |                                            |FM-8872  |    53|FM-8872-53 |CUSTODIAN_ADDRESS_ZIP_CODE  |
|CUSTODIAN ADDRESS ZIP EXT   |4               |                            |AlphaNumeric |                                            |FM-8872  |    55|FM-8872-55 |CUSTODIAN_ADDRESS_ZIP_EXT   |
|CONTACT PERSON NAME         |50              |                            |AlphaNumeric |                                            |FM-8872  |    57|FM-8872-57 |CONTACT_PERSON_NAME         |
|CONTACT ADDRESS 1           |50              |                            |AlphaNumeric |                                            |FM-8872  |    59|FM-8872-59 |CONTACT_ADDRESS_1           |
|CONTACT ADDRESS 2           |50              |                            |AlphaNumeric |                                            |FM-8872  |    61|FM-8872-61 |CONTACT_ADDRESS_2           |
|CONTACT ADDRESS CITY        |50              |                            |AlphaNumeric |                                            |FM-8872  |    63|FM-8872-63 |CONTACT_ADDRESS_CITY        |
|CONTACT ADDRESS STATE       |2               |                            |AlphaNumeric |                                            |FM-8872  |    65|FM-8872-65 |CONTACT_ADDRESS_STATE       |
|CONTACT ADDRESS ZIP CODE    |5               |                            |AlphaNumeric |                                            |FM-8872  |    67|FM-8872-67 |CONTACT_ADDRESS_ZIP_CODE    |
|CONTACT ADDRESS ZIP EXT     |4               |                            |AlphaNumeric |                                            |FM-8872  |    69|FM-8872-69 |CONTACT_ADDRESS_ZIP_EXT     |
|BUSINESS ADDRESS 1          |50              |                            |AlphaNumeric |                                            |FM-8872  |    71|FM-8872-71 |BUSINESS_ADDRESS_1          |
|BUSINESS ADDRESS 2          |50              |                            |AlphaNumeric |                                            |FM-8872  |    73|FM-8872-73 |BUSINESS_ADDRESS_2          |
|BUSINESS ADDRESS CITY       |50              |                            |AlphaNumeric |                                            |FM-8872  |    75|FM-8872-75 |BUSINESS_ADDRESS_CITY       |
|BUSINESS ADDRESS STATE      |2               |                            |AlphaNumeric |                                            |FM-8872  |    77|FM-8872-77 |BUSINESS_ADDRESS_STATE      |
|BUSINESS ADDRESS ZIP CODE   |5               |                            |AlphaNumeric |                                            |FM-8872  |    79|FM-8872-79 |BUSINESS_ADDRESS_ZIP_CODE   |
|BUSINESS ADDRESS ZIP EXT    |4               |                            |AlphaNumeric |                                            |FM-8872  |    81|FM-8872-81 |BUSINESS_ADDRESS_ZIP_EXT    |
|QTR INDICATOR               |1               |1  to  8                    |Alphanumeric |1 = First Quarterly                         |FM-8872  |    83|FM-8872-83 |QTR_INDICATOR               |
|                            |                |                            |             |2 = Second Quarterly                        |FM-8872  |    84|FM-8872-84 |                            |
|                            |                |                            |             |3 = Third Quarterly 4 = Year-end            |FM-8872  |    85|FM-8872-85 |                            |
|                            |                |                            |             |5 = Mid-Year                                |FM-8872  |    86|FM-8872-86 |                            |
|                            |                |                            |             |6 = Monthly                                 |FM-8872  |    87|FM-8872-87 |                            |
|                            |                |                            |             |7 = Pre-election                            |FM-8872  |    88|FM-8872-88 |                            |
|                            |                |                            |             |8 = Post-election                           |FM-8872  |    89|FM-8872-89 |                            |
|                            |                |                            |             |                                            |FM-8872  |    90|FM-8872-90 |                            |
|MONTHLY RPT MONTH           |2               |If Monthly; 1-12; else NULL |AlphaNumeric |If QTR Indicator - Monthly; Month is filled |FM-8872  |    92|FM-8872-92 |MONTHLY_RPT_MONTH           |
|PRE ELECT TYPE              |10              |If PreElect; Else Null      |AlphaNumeric |Null if this is a post election rpt         |FM-8872  |    94|FM-8872-94 |PRE_ELECT_TYPE              |
|PRE or POST ELECT DATE      |8               |                            |AlphaNumeric |                                            |FM-8872  |    96|FM-8872-96 |PRE_OR_POST_ELECT_DATE      |
|PRE or POST ELECT STATE     |2               |                            |AlphaNumeric |                                            |FM-8872  |    98|FM-8872-98 |PRE_OR_POST_ELECT_STATE     |
|SCHED_A_IND                 |1               |1 or 0                      |AlphaNumeric |1 = No Sched A                              |FM-8872  |   100|FM-8872-00 |SCHED_A_IND                 |
|                            |                |                            |             |0 = Sched A exists                          |FM-8872  |   101|FM-8872-01 |                            |
|TOTAL_SCHED_A               |19              |                            |numeric      |                                            |FM-8872  |   103|FM-8872-03 |TOTAL_SCHED_A               |
|SCHED_B_IND                 |1               |1 or 0                      |AlphaNumeric |1 = No Sched B                              |FM-8872  |   105|FM-8872-05 |SCHED_B_IND                 |
|                            |                |                            |             |0 = Sched B exists                          |FM-8872  |   106|FM-8872-06 |                            |
|TOTAL_SCHED_B               |19              |                            |numeric      |                                            |FM-8872  |   108|FM-8872-08 |TOTAL_SCHED_B               |
|INSERT_DATETIME             |19              |YYYY-MM-DD HH24:MI:SS       |Datetime     |                                            |FM-8872  |   110|FM-8872-10 |INSERT_DATETIME             |





### SCHED-A


|IRS_FIELD_NAME               |SIZE            |VALID_VALUES |FORMAT       |DESCRIPTION                                                  |FORMTYPE | ORDER|F_ORDER    |VARNAME                      |
|:----------------------------|:---------------|:------------|:------------|:------------------------------------------------------------|:--------|-----:|:----------|:----------------------------|
|Record Type                  |1               |A            |Alphanumeric |Designates Schedule A Record that relates to an 8872 Form ID |SCHED-A  |     1|SCHED-A-01 |RECORD_TYPE                  |
|Form ID Number               |Up to 38 digits |             |Numeric      |                                                             |SCHED-A  |     3|SCHED-A-03 |FORM_ID_NUMBER               |
|SCHED A ID                   |Up to 38 digits |             |Numeric      |                                                             |SCHED-A  |     5|SCHED-A-05 |SCHED_A_ID                   |
|ORG NAME                     |70              |             |AlphaNumeric |                                                             |SCHED-A  |     7|SCHED-A-07 |ORG_NAME                     |
|EIN                          |9               |             |AlphaNumeric |                                                             |SCHED-A  |     9|SCHED-A-09 |EIN                          |
|CONTRIBUTOR NAME             |50              |             |AlphaNumeric |                                                             |SCHED-A  |    11|SCHED-A-11 |CONTRIBUTOR_NAME             |
|CONTRIBUTOR ADDRESS 1        |50              |             |AlphaNumeric |                                                             |SCHED-A  |    13|SCHED-A-13 |CONTRIBUTOR_ADDRESS_1        |
|CONTRIBUTOR ADDRESS 2        |50              |             |AlphaNumeric |                                                             |SCHED-A  |    15|SCHED-A-15 |CONTRIBUTOR_ADDRESS_2        |
|CONTRIBUTOR ADDRESS CITY     |50              |             |AlphaNumeric |                                                             |SCHED-A  |    17|SCHED-A-17 |CONTRIBUTOR_ADDRESS_CITY     |
|CONTRIBUTOR ADDRESS STATE    |2               |             |AlphaNumeric |                                                             |SCHED-A  |    19|SCHED-A-19 |CONTRIBUTOR_ADDRESS_STATE    |
|CONTRIBUTOR ADDRESS ZIP CODE |5               |             |AlphaNumeric |                                                             |SCHED-A  |    21|SCHED-A-21 |CONTRIBUTOR_ADDRESS_ZIP_CODE |
|CONTRIBUTOR ADDRESS ZIP EXT  |4               |             |AlphaNumeric |                                                             |SCHED-A  |    23|SCHED-A-23 |CONTRIBUTOR_ADDRESS_ZIP_EXT  |
|CONTRIBUTOR EMPLOYER         |70              |             |AlphaNumeric |                                                             |SCHED-A  |    25|SCHED-A-25 |CONTRIBUTOR_EMPLOYER         |
|CONTRIBUTION AMOUNT          |17              |             |AlphaNumeric |                                                             |SCHED-A  |    27|SCHED-A-27 |CONTRIBUTION_AMOUNT          |
|CONTRIBUTOR OCCUPATION       |70              |             |AlphaNumeric |                                                             |SCHED-A  |    29|SCHED-A-29 |CONTRIBUTOR_OCCUPATION       |
|AGG CONTRIBUTION YTD         |17              |             |AlphaNumeric |                                                             |SCHED-A  |    31|SCHED-A-31 |AGG_CONTRIBUTION_YTD         |
|CONTRIBUTION DATE            |8               |             |AlphaNumeric |                                                             |SCHED-A  |    33|SCHED-A-33 |CONTRIBUTION_DATE            |

### SCHED-B


|IRS_FIELD_NAME              |SIZE            |VALID_VALUES |FORMAT       |DESCRIPTION                                                  |FORMTYPE | ORDER|F_ORDER    |VARNAME                     |
|:---------------------------|:---------------|:------------|:------------|:------------------------------------------------------------|:--------|-----:|:----------|:---------------------------|
|Record Type                 |1               |B            |Alphanumeric |Designates Schedule B Record that relates to an 8872 Form ID |SCHED-B  |     1|SCHED-B-01 |RECORD_TYPE                 |
|Form ID Number              |Up to 38 digits |             |Numeric      |                                                             |SCHED-B  |     3|SCHED-B-03 |FORM_ID_NUMBER              |
|SCHED B ID                  |Up to 38 digits |             |Numeric      |                                                             |SCHED-B  |     5|SCHED-B-05 |SCHED_B_ID                  |
|ORG NAME                    |70              |             |AlphaNumeric |                                                             |SCHED-B  |     7|SCHED-B-07 |ORG_NAME                    |
|EIN                         |9               |             |AlphaNumeric |                                                             |SCHED-B  |     9|SCHED-B-09 |EIN                         |
|RECIEPIENT NAME             |50              |             |AlphaNumeric |                                                             |SCHED-B  |    11|SCHED-B-11 |RECIEPIENT_NAME             |
|RECIEPIENT ADDRESS 1        |50              |             |AlphaNumeric |                                                             |SCHED-B  |    13|SCHED-B-13 |RECIEPIENT_ADDRESS_1        |
|RECIEPIENT ADDRESS 2        |50              |             |AlphaNumeric |                                                             |SCHED-B  |    15|SCHED-B-15 |RECIEPIENT_ADDRESS_2        |
|RECIEPIENT ADDRESS CITY     |50              |             |AlphaNumeric |                                                             |SCHED-B  |    17|SCHED-B-17 |RECIEPIENT_ADDRESS_CITY     |
|RECIEPIENT ADDRESS ST       |2               |             |AlphaNumeric |                                                             |SCHED-B  |    19|SCHED-B-19 |RECIEPIENT_ADDRESS_ST       |
|RECIEPIENT ADDRESS ZIP CODE |5               |             |AlphaNumeric |                                                             |SCHED-B  |    21|SCHED-B-21 |RECIEPIENT_ADDRESS_ZIP_CODE |
|RECIEPIENT ADDRESS ZIP EXT  |4               |             |AlphaNumeric |                                                             |SCHED-B  |    23|SCHED-B-23 |RECIEPIENT_ADDRESS_ZIP_EXT  |
|RECIEPIENT EMPLOYER         |70              |             |AlphaNumeric |                                                             |SCHED-B  |    25|SCHED-B-25 |RECIEPIENT_EMPLOYER         |
|EXPENDITURE AMOUNT          |17              |             |AlphaNumeric |                                                             |SCHED-B  |    27|SCHED-B-27 |EXPENDITURE_AMOUNT          |
|RECIPIENT OCCUPATION        |70              |             |AlphaNumeric |                                                             |SCHED-B  |    29|SCHED-B-29 |RECIPIENT_OCCUPATION        |
|EXPENDITURE DATE            |8               |             |AlphaNumeric |                                                             |SCHED-B  |    31|SCHED-B-31 |EXPENDITURE_DATE            |
|EXPENDITURE PURPOSE         |512             |             |AlphaNumeric |                                                             |SCHED-B  |    33|SCHED-B-33 |EXPENDITURE_PURPOSE         |





## Metadata


### HEADER


|IRS_FIELD_NAME    |SIZE     |VALID_VALUES                              |FORMAT       |DESCRIPTION                                                                                                                                                     |FORMTYPE | ORDER|F_ORDER   |VARNAME           |
|:-----------------|:--------|:-----------------------------------------|:------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------|-----:|:---------|:-----------------|
|Record Type Code  |1        |H                                         |Character    |Designates a file header                                                                                                                                        |HEADER   |     1|HEADER-01 |RECORD_TYPE_CODE  |
|Transmission Date |-8       |SYSDATE                                   |Alphanumeric |Date file is created                                                                                                                                            |HEADER   |     3|HEADER-03 |TRANSMISSION_DATE |
|                  |yyyymmdd |                                          |             |                                                                                                                                                                |HEADER   |     4|HEADER-04 |                  |
|Transmission Time |-4       |SYSDATE                                   |Alphanumeric |Time file is created                                                                                                                                            |HEADER   |     6|HEADER-06 |TRANSMISSION_TIME |
|                  |hhmm     |                                          |             |                                                                                                                                                                |HEADER   |     7|HEADER-07 |                  |
|File ID Modifier  |-1       |A for first part of alphabet transmission |Character    |This designates the file that the user downloaded.  The user has the option to download a full data file; or separate smaller data files broken up by alphabet. |HEADER   |     9|HEADER-09 |FILE_ID_MODIFIER  |
|                  |         |B for second transmission                 |             |                                                                                                                                                                |HEADER   |    10|HEADER-10 |                  |
|                  |         |C for third transmission                  |             |                                                                                                                                                                |HEADER   |    11|HEADER-11 |                  |
|                  |         |D for fourth transmission                 |             |                                                                                                                                                                |HEADER   |    12|HEADER-12 |                  |
|                  |         |F for full data transmission              |             |                                                                                                                                                                |HEADER   |    13|HEADER-13 |                  |



### FOOTER


|IRS_FIELD_NAME    |SIZE     |VALID_VALUES |FORMAT       |DESCRIPTION                       |FORMTYPE | ORDER|F_ORDER   |VARNAME           |
|:-----------------|:--------|:------------|:------------|:---------------------------------|:--------|-----:|:---------|:-----------------|
|Record Type Code  |1        |F            |Character    |Designates a file header          |FOOTER   |     1|FOOTER-01 |RECORD_TYPE_CODE  |
|Transmission Date |8        |SYSDATE      |Alphanumeric |Date on which the file is created |FOOTER   |     3|FOOTER-03 |TRANSMISSION_DATE |
|                  |yyyymmdd |             |             |                                  |FOOTER   |     4|FOOTER-04 |                  |
|Transmission Time |4        |SYSDATE      |Alphanumeric |Time when file is created         |FOOTER   |     6|FOOTER-06 |TRANSMISSION_TIME |
|Record Count      |20       |             |Numeric      |                                  |FOOTER   |     8|FOOTER-08 |RECORD_COUNT      |



<br>

<hr>

<br>


```{=html}
<style>


h1.title {
 font-size: 60px;
 color: #0a4c6a;
}


h4, .h4 {
    font-size: 40px;
    color: #1696d2;
    margin-bottom: 50px;
}



.button {
  background-color: white;
  color:  #12719e;
  border: 2px solid  #12719e;   /* #008CBA; */
  padding: 5px 10px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  border-radius: 12px;
  width: 150px;
}
 
.button {
  transition-duration: 0.4s;
}

.button:hover {
  background-color: #1696d2; 
  color: white;
  border: 2px solid #12719e;
}


.button2 {
  background-color: white;
  color: #12719e;
  border: 2px solid #9d9d9d;   /* #008CBA; */
  padding: 5px 10px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  border-radius: 12px;
  width: 150px;
}

.button2 {
  transition-duration: 0.4s;
}

.button2:hover {
  background-color: #fff2cf; 
  color: #1696d2;
  font-weight: bold;
  border: 2px solid #1696d2;
}


.center {text-align: center;}

table td {
  vertical-align: middle;
}

blockquote {
    border-left: 4px solid #1696d2;
    margin-left: 10px;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding: 15px;
}

.button3 {
  background-color: #0a4c6a;
  color: white;
  border: 2px solid #0a4c6a;   
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  border-radius: 4px;
  width: 100px;
}
</style>
```

