# Input data anlysis tool
Team project for Credit Suisse realized as part of my studies.

The premise of our project is to create a tool that will compare the structure and type of incoming data sets. The data sets will be inputted in CSV formats and are intended to be compared with the patterns contained in both the main DDA file and the individual one for each incoming CSV file. Each detected error should return a warning.
# Assumptions
- Files sent for verification must be compressed in .tar format
- The program assumes that all input data is provided in the appropriate format, as specified in the DDA JSON files
- If an error occurs in the checked data column, it is returned, and the column is not further checked
- The program asks the user for the path to the input file
- The program retrieves the names of the required data sets from the main DDA file and validates the correctness of those accepted from the user
- The program retrieves the structure of a specific data set in JSON format and confronts it with the submitted datasets in CSV format
- The program searches for possible errors and returns all warnings in the logger

# Input
As input program takes path to .tar archive that contains .csv files. Path to DDA JSON files is currently hard-coded

![image](https://github.com/plmrr/input-data-anlysis-tool/assets/130595899/5f1cbe74-0cf8-47e8-9e07-156b15723f77)

# Output
The program returns .log file containing occured erros for each dataset

```
WARNING:comparing:There is missing file debt_bb_pr.csv
WARNING:comparing:There is missing file eq_bb_pr.csv
WARNING:comparing:There is missing file trader.csv
WARNING:comparing:There is missing file fb_trader.csv
WARNING:comparing:There is missing file fx_shredder.csv
WARNING:comparing:There is missing file GFX_Spot.csv
WARNING:comparing:There is missing file eq_rt_pr.csv
WARNING:comparing:There is missing file reference_entity.csv
WARNING:comparing:There is missing file sdata_commodity.csv
WARNING:comparing:There is missing file eq_rt_pr_adj_factor.csv
WARNING:comparing:There are wrong value types in following rows [0, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99] in LABEL in trader_cds_price.csv, should be DATE with DD-MMM-YYYY format
WARNING:comparing:Wrong value type in BID in trader_cds_price.csv. Correct type is DOUBLE
WARNING:comparing:There are wrong value types in following rows [1] in BID in trader_cds_price.csv
WARNING:comparing:Wrong value type in SYNTHETIC in trader_cds_price.csv. Correct type is INTEGER
WARNING:comparing:There are wrong value types in following rows [8] in SYNTHETIC in trader_cds_price.csv
WARNING:comparing:Wrong value type in MDS_CHAIN_ORDER in trader_cds_price.csv. Correct type is INTEGER
WARNING:comparing:There are wrong value types in following rows [0] in MDS_CHAIN_ORDER in trader_cds_price.csv
WARNING:comparing:There are wrong value types in following rows [0] in MDS_DATE in trader_cds_price.csv, should be DATE with yyyy-MM-dd format
```

# Extended documentation
ENG: [Documentation_ENG.pdf](https://github.com/plmrr/input-data-anlysis-tool/files/11962446/Documentation_ENG.pdf)

PL: [Dokumentacja_PL.pdf](https://github.com/plmrr/input-data-anlysis-tool/files/11962447/Dokumentacja_PL.pdf)

Usage of ChatGPT: [ChatGPT- short summary.pdf](https://github.com/plmrr/input-data-anlysis-tool/files/11962462/ChatGPT-.short.summary.pdf)
