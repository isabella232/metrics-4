# metrics repo

Regularly collect and log metrics about IPFS related projects.

This repo contains a scheduled GitHub Action which pulls IPFS dependency data out of BigQuery and stores it 
in [timestamped json](./logs) files in this repo.

## Recent Data

### Google Trends

We're collecting the "interest over time" metric from Google Trends. From Google *"Numbers 
represent search interest relative to the highest point on the chart for the given region and 
time. A value of 100 is the peak popularity for the term. A value of 50 means that the term is 
half as popular. Likewise a score of 0 means the term was less than 1% as popular as the peak."*

This is the google trend data for searches of the term "IPFS" for the
last 12 months. The last 10 years is [available here.](./results/google-trends.md)



Google Trends:
*  4/2020: 64
*  3/2020: 56
*  2/2020: 57
*  1/2020: 63
*  12/2019: 59
*  11/2019: 56
*  10/2019: 61
*  9/2019: 59
*  8/2019: 65
*  7/2019: 69
*  6/2019: 73
*  5/2019: 81

### GitHub Search

These do a repository search, filtered by language, for "ipfs." This search
finds references to ipfs in project names, descriptions, and anything else
GitHub finds relevant (this isn't actually documented very well by GitHub).

GitHub limits the maximum results to 1K. We can get around this a little bit
by performing additional queries w/ different sorts in ascending and descending
order, but there's some amount we'll never get. That's why it's nice to have
the historical data logged in the repo every day.

The "total matches" we get is larger than the result set, even when the result
set is below the 1K limit imposed by GitHub. This isn't documented sufficiently
so we don't know why this is the case.

#### Go Repositories

Total Matches: 1555

Total Results (Limited by GitHUB API): 311

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [mborho/terraform-provider-ipfs](https://github.com/mborho/terraform-provider-ipfs)| 2 | 0 | 26| 2020-04-09 | 2020-04-09 |
| [itzg/go-ipfs-client](https://github.com/itzg/go-ipfs-client)| 0 | 0 | 30| 2020-04-05 | 2020-04-05 |
| [dbarasti/go-monitor-ipfs](https://github.com/dbarasti/go-monitor-ipfs)| 1 | 0 | 10169| 2020-04-03 | 2020-04-10 |
| [alanshaw/ipfs-hookds](https://github.com/alanshaw/ipfs-hookds)| 2 | 0 | 19| 2020-03-31 | 2020-04-08 |
| [RTradeLtd/ipld-eml](https://github.com/RTradeLtd/ipld-eml)| 5 | 0 | 42700| 2020-03-27 | 2020-03-30 |
| [RTradeLtd/go-temporalx-sdk](https://github.com/RTradeLtd/go-temporalx-sdk)| 3 | 0 | 103| 2020-03-26 | 2020-04-10 |
| [RTradeLtd/ipcoronafs](https://github.com/RTradeLtd/ipcoronafs)| 2 | 1 | 28327| 2020-03-23 | 2020-03-23 |
| [jolatechno/mpi-peerstore](https://github.com/jolatechno/mpi-peerstore)| 0 | 0 | 61| 2020-03-21 | 2020-03-30 |
| [RTradeLtd/iprfc](https://github.com/RTradeLtd/iprfc)| 1 | 0 | 63| 2020-03-19 | 2020-03-19 |
| [Wondertan/go-blockstream](https://github.com/Wondertan/go-blockstream)| 1 | 0 | 45| 2020-03-11 | 2020-04-11 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 69600

Total Results (Limited by GitHUB API): 1272

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [ferru97/node-ipfs-monitor](https://github.com/ferru97/node-ipfs-monitor)| 0 | 0 | 102| 2020-04-09 | 2020-04-11 |
| [moebiusprogram/notarize-api](https://github.com/moebiusprogram/notarize-api)| 0 | 0 | 707| 2020-04-07 | 2020-04-10 |
| [BhaskarDutta2209/Meme_Of_The_Day](https://github.com/BhaskarDutta2209/Meme_Of_The_Day)| 0 | 0 | 251| 2020-04-07 | 2020-04-07 |
| [rubcv/IPFS-API](https://github.com/rubcv/IPFS-API)| 0 | 0 | 28| 2020-04-07 | 2020-04-07 |
| [luisvid/IPFS-SmartContract](https://github.com/luisvid/IPFS-SmartContract)| 0 | 0 | 346| 2020-04-02 | 2020-04-02 |
| [zemse/decentralised-registration-ipfs](https://github.com/zemse/decentralised-registration-ipfs)| 0 | 0 | 3503| 2020-03-30 | 2020-04-08 |
| [tabcat/ipfs-serve](https://github.com/tabcat/ipfs-serve)| 0 | 0 | 9| 2020-03-26 | 2020-03-27 |
| [sanketpathak64/file-upload-using-IPFS](https://github.com/sanketpathak64/file-upload-using-IPFS)| 0 | 0 | 288| 2020-03-24 | 2020-03-26 |
| [denismp/mi4-exercise8-2](https://github.com/denismp/mi4-exercise8-2)| 0 | 0 | 2580| 2020-03-24 | 2020-03-26 |
| [ariels1996/KOK-dApp-demo](https://github.com/ariels1996/KOK-dApp-demo)| 0 | 0 | 324| 2020-03-24 | 2020-04-06 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
