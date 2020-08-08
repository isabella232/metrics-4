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
*  8/2020: 58
*  7/2020: 73
*  6/2020: 73
*  5/2020: 70
*  4/2020: 67
*  3/2020: 62
*  2/2020: 63
*  1/2020: 60
*  12/2019: 62
*  11/2019: 57
*  10/2019: 64
*  9/2019: 58

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

Total Matches: 1775

Total Results (Limited by GitHUB API): 355

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [zot/textcraft-treerequest](https://github.com/zot/textcraft-treerequest)| 0 | 0 | 41| 2020-08-04 | 2020-08-04 |
| [grufwub/gibon](https://github.com/grufwub/gibon)| 2 | 0 | 191| 2020-08-03 | 2020-08-07 |
| [decentralized-identity/go-ipfs-ds-azure](https://github.com/decentralized-identity/go-ipfs-ds-azure)| 0 | 0 | 60| 2020-07-31 | 2020-08-07 |
| [gioapp/ipfs](https://github.com/gioapp/ipfs)| 0 | 0 | 4228| 2020-07-22 | 2020-08-06 |
| [wabarc/ipfs-pinner](https://github.com/wabarc/ipfs-pinner)| 0 | 0 | 17| 2020-07-18 | 2020-07-18 |
| [aschmahmann/ipfs-ds](https://github.com/aschmahmann/ipfs-ds)| 2 | 0 | 57| 2020-07-16 | 2020-07-16 |
| [diviramon/vbeam](https://github.com/diviramon/vbeam)| 3 | 1 | 262| 2020-07-06 | 2020-08-07 |
| [wabarc/wbipfs](https://github.com/wabarc/wbipfs)| 0 | 0 | 9682| 2020-07-04 | 2020-07-18 |
| [BDWare/go-ipfs](https://github.com/BDWare/go-ipfs)| 0 | 0 | 40531| 2020-07-01 | 2020-07-01 |
| [RTradeLtd/go-ipfs-sharedforeststore](https://github.com/RTradeLtd/go-ipfs-sharedforeststore)| 4 | 0 | 260| 2020-06-25 | 2020-08-03 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 72999

Total Results (Limited by GitHUB API): 1303

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [spsingh559/ipfs-eth](https://github.com/spsingh559/ipfs-eth)| 0 | 0 | 101| 2020-08-07 | 2020-08-07 |
| [GremApp/ExpressAPI](https://github.com/GremApp/ExpressAPI)| 0 | 0 | 43625| 2020-08-03 | 2020-08-03 |
| [GustaveNimant/irp_ipfs_full](https://github.com/GustaveNimant/irp_ipfs_full)| 0 | 0 | 93| 2020-08-02 | 2020-08-06 |
| [myst33d/IPFSUpload](https://github.com/myst33d/IPFSUpload)| 0 | 0 | 29| 2020-08-02 | 2020-08-03 |
| [rakaar/ipfs-logger](https://github.com/rakaar/ipfs-logger)| 0 | 0 | 88| 2020-08-01 | 2020-08-01 |
| [Permissionless-Software-Foundation/bch-w...](https://github.com/Permissionless-Software-Foundation/bch-wallet-plugin-postoffice)| 1 | 0 | 660| 2020-08-01 | 2020-08-07 |
| [oya-protocol/hackfs](https://github.com/oya-protocol/hackfs)| 1 | 0 | 1729| 2020-07-31 | 2020-08-07 |
| [devbootstrap/IPFS-vuejs-drizzle-app](https://github.com/devbootstrap/IPFS-vuejs-drizzle-app)| 0 | 0 | 130| 2020-07-29 | 2020-07-29 |
| [ARNiroula/test_ipfsnode](https://github.com/ARNiroula/test_ipfsnode)| 0 | 0 | 4645| 2020-07-28 | 2020-08-05 |
| [Sebastian-Gru/ipfs-prototype-spielereien](https://github.com/Sebastian-Gru/ipfs-prototype-spielereien)| 0 | 0 | 344| 2020-07-28 | 2020-07-29 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
