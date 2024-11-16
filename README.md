# Blood Bowl 3 matches data extractor
## Goals and Objectives
To get Blood Bowl 3 matches raw data, for playing with it. Code fetches raw matches statistics from given competition using Cyanide API.

## Stack
Python 3.12.4 (pandas, requests, pathlib)

## Workflow
For getting data we should have a key for Cyanide API, find needed competition ID and define several parameters (like chunk size or request limit).

Code extracts data chunk by chunk, if something breaks - saves extracted data to temporary file and can be restarted later and continue from this point (no need to start extracting from the beginning).

## Results
If something breaks mid-process, we have 'temporary.csv' file with partial data. After restarting code it will continue extracting data from this point.

After completing data fetching we have csv-file '{competition_name}_{platform}_raw_data.csv' with all raw matches data from given competition.
