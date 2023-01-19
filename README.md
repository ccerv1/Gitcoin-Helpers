# Gitcoin-Helpers

Starting to collect little scripts which may be helpful when working with Gitcoin Data and Protocol. Contributions welcome!

## GetGrantsData.py
This script takes a round ID and API_KEY (your API_KEY for querying TheGraph protocol) as input and returns data on the projects in the round, primarily the projects title and payout_address. Data is gathered from the mainnet subgraph and IPFS. The output comes in two forms: a csv file and a SQL file. The SQL file can be used to start a Dune Query.

## create_hypercerts_metadata.py
This script takes as arguments:
1. The path of a csv file created by `GetGrantsData.py` 
2. A directory for exporting hypercerts metadata (as a json), eg, `../metadata/myround`
It tranforms the data in the csv file into a metadata file (ready for uploading on IPFS) that stores all required hypercerts properties