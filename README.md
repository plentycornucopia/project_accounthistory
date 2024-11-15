# Project: Account History
Project: Account History

We need to store all **account history** records on our personal budget from month to month. We want to store them in a Postgres DB with the following column structure:

|Reference|Report Date|Group|Type|ChesterPA|AllenTX|AtlantaGA|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|*VARCHAR(9)|*MM/DD/YYYY|VARCHAR(3)|VARCHAR(255)|VARCHAR(255)|VARCHAR(255)|VARCHAR(255)|

* From month to month we will not know how many inquiry records we'll have. Could be 1. Could 30. Could be 0.
* If 0, no record should be created. If ≤1, then create the corresponding record(s) in the DB.

*must always be present

**may sometimes be blank

***postgres db available upon request

## Group Selector
`#ctrlCreditReport > chesterpa-report > div.ng-binding.ng-scope > div:nth-child(12) > div:nth-child(3) > address-history > div`

## First Object Selector
`#ctrlCreditReport > chesterpa-report > div.ng-binding.ng-scope > div:nth-child(12) > div:nth-child(3) > address-history > div > ng-repeat:nth-child(1)`
