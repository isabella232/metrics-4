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
*  8/2020: 60
*  7/2020: 72
*  6/2020: 69
*  5/2020: 64
*  4/2020: 65
*  3/2020: 58
*  2/2020: 56
*  1/2020: 59
*  12/2019: 58
*  11/2019: 60
*  10/2019: 62
*  9/2019: 59

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

Total Matches: 1780

Total Results (Limited by GitHUB API): 356

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [zot/textcraft-treerequest](https://github.com/zot/textcraft-treerequest)| 0 | 0 | 93| 2020-08-04 | 2020-08-18 |
| [grufwub/gibon](https://github.com/grufwub/gibon)| 3 | 0 | 191| 2020-08-03 | 2020-08-07 |
| [decentralized-identity/go-ipfs-ds-azure](https://github.com/decentralized-identity/go-ipfs-ds-azure)| 0 | 0 | 68| 2020-07-31 | 2020-08-19 |
| [gioapp/ipfs](https://github.com/gioapp/ipfs)| 0 | 0 | 4228| 2020-07-22 | 2020-08-06 |
| [wabarc/ipfs-pinner](https://github.com/wabarc/ipfs-pinner)| 0 | 0 | 19| 2020-07-18 | 2020-08-10 |
| [aschmahmann/ipfs-ds](https://github.com/aschmahmann/ipfs-ds)| 2 | 1 | 57| 2020-07-16 | 2020-07-16 |
| [Wondertan/go-ipfs-recovery](https://github.com/Wondertan/go-ipfs-recovery)| 6 | 2 | 76| 2020-07-11 | 2020-08-18 |
| [diviramon/vbeam](https://github.com/diviramon/vbeam)| 3 | 1 | 263| 2020-07-06 | 2020-08-14 |
| [wabarc/wbipfs](https://github.com/wabarc/wbipfs)| 0 | 0 | 9749| 2020-07-04 | 2020-08-15 |
| [BDWare/go-ipfs](https://github.com/BDWare/go-ipfs)| 0 | 0 | 40531| 2020-07-01 | 2020-07-01 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 73598

Total Results (Limited by GitHUB API): 1330

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [holtolee/holtolee.github.io](https://github.com/holtolee/holtolee.github.io)| 0 | 0 | 3573| 2020-08-19 | 2020-08-19 |
| [KYCCrypto/ipfs-crypt](https://github.com/KYCCrypto/ipfs-crypt)| 1 | 0 | 16| 2020-08-15 | 2020-08-15 |
| [kay404/ipfs-cluster-mini](https://github.com/kay404/ipfs-cluster-mini)| 0 | 0 | 73| 2020-08-13 | 2020-08-13 |
| [indahud/ipfs-file-upload](https://github.com/indahud/ipfs-file-upload)| 0 | 0 | 17| 2020-08-12 | 2020-08-12 |
| [tgrecojs/nextjs-fleek](https://github.com/tgrecojs/nextjs-fleek)| 0 | 0 | 17098| 2020-08-09 | 2020-08-10 |
| [narojishubham/ipfs-demo](https://github.com/narojishubham/ipfs-demo)| 0 | 0 | 15| 2020-08-08 | 2020-08-08 |
| [spsingh559/ipfs-eth](https://github.com/spsingh559/ipfs-eth)| 0 | 0 | 101| 2020-08-07 | 2020-08-07 |
| [sleepycharlyy/tic2bar.js](https://github.com/sleepycharlyy/tic2bar.js)| 3 | 0 | 29249| 2020-08-06 | 2020-08-10 |
| [GremApp/ExpressAPI](https://github.com/GremApp/ExpressAPI)| 0 | 0 | 43625| 2020-08-03 | 2020-08-03 |
| [GustaveNimant/irp_ipfs_full](https://github.com/GustaveNimant/irp_ipfs_full)| 0 | 0 | 120| 2020-08-02 | 2020-08-15 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
