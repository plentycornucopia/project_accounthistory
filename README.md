# Project: Account History

## Description of Project
We need a PHP solution to parse this HTML file uploaded by our family members. Each file will follow the same format, but the number of records inside may vary. Parsed data will be saved into a PostgreSQL database.

## Requirements
* validate file size
* validate by HTML MIME type
* temporary storage can be used but must be terminated after successful storage
* delivered file needs to independently function without the assistance of frameworks
* vanilla PHP is the only acceptable approach
* no frameworks to be used (like Laravel or Slim)

We need to store all **Account History** records on our personal budget from month to month. We want to store them in a Postgres DB with the following column structure:

|Reference|Report Date|Group|Subproup|Type|ChesterPA|AllenTX|AtlantaGA|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|*VARCHAR(9)|*MM/DD/YYYY|VARCHAR(255)|VARCHAR(255)|VARCHAR(255)|VARCHAR(255)|VARCHAR(255)|VARCHAR(255)|

* From month to month we will not know how many inquiry records we'll have. Could be 1. Could 30. Could be 0.
* If 0, no record should be created. If ≤1, then create the corresponding record(s) in the DB.

*must always be present

**may sometimes be blank

***postgres db available upon request

## Screenshot of Data Table in HTML
![Table Appears in HTML](file%20to%20be%20parsed-%20accounthistory.png?raw=true "Table Appears in HTML")

## Data Once Inputed to Postgres
|Reference|Report Date|Group|Subgroup|Type|ChesterPA|AllenTX|AtlantaGA|
|:-:|:-:|:-:|:-:|:-:|:-:|
|BR54898847|05/23/2024|AZ/ SYNCB/PPMC|000|JSON|JSON|JSON|

## Screenshot of Reference Table
![Table Appears in HTML](accounthistory_reference.png?raw=true "Table Appears in HTML")

## Group Selector
`#ctrlCreditReport > chesterpa-report > div.ng-binding.ng-scope > div:nth-child(12) > div:nth-child(3) > address-history > div`

## First Object Selector
`#ctrlCreditReport > chesterpa-report > div.ng-binding.ng-scope > div:nth-child(12) > div:nth-child(3) > address-history > div > ng-repeat:nth-child(1)`
