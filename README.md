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
*  3/2020: 54
*  2/2020: 59
*  1/2020: 62
*  12/2019: 52
*  11/2019: 59
*  10/2019: 61
*  9/2019: 59
*  8/2019: 66
*  7/2019: 63
*  6/2019: 72
*  5/2019: 76
*  4/2019: 72

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

Total Matches: 1515

Total Results (Limited by GitHUB API): 303

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [dzhelezov/ipfs-crawler](https://github.com/dzhelezov/ipfs-crawler)| 0 | 0 | 33| 2020-03-05 | 2020-03-05 |
| [jolatechno/ipfs-compute](https://github.com/jolatechno/ipfs-compute)| 0 | 0 | 46| 2020-03-04 | 2020-03-09 |
| [jolatechno/ipfs-compute-plugin](https://github.com/jolatechno/ipfs-compute-plugin)| 0 | 0 | 93| 2020-03-03 | 2020-03-09 |
| [GalaIO/P2Pcrawler](https://github.com/GalaIO/P2Pcrawler)| 0 | 0 | 82| 2020-03-03 | 2020-03-09 |
| [sencvkk/go-ipfs](https://github.com/sencvkk/go-ipfs)| 0 | 0 | 100440| 2020-03-03 | 2020-03-09 |
| [TRON-US/btfs-migration-toolkit](https://github.com/TRON-US/btfs-migration-toolkit)| 0 | 0 | 21039| 2020-02-10 | 2020-02-21 |
| [zot/ipfs-p2p-websocket](https://github.com/zot/ipfs-p2p-websocket)| 0 | 0 | 21888| 2020-02-05 | 2020-02-27 |
| [likecoin/iscn-ipld](https://github.com/likecoin/iscn-ipld)| 0 | 0 | 46| 2020-02-03 | 2020-03-02 |
| [sug0/go-ipfs-boards](https://github.com/sug0/go-ipfs-boards)| 0 | 0 | 21| 2020-01-28 | 2020-02-10 |
| [simpleaswater/twitter-pinbot](https://github.com/simpleaswater/twitter-pinbot)| 4 | 0 | 47| 2020-01-19 | 2020-01-23 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 68600

Total Results (Limited by GitHUB API): 1256

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [PinataCloud/ipfs-node-connection-handler](https://github.com/PinataCloud/ipfs-node-connection-handler)| 1 | 0 | 17| 2020-03-03 | 2020-03-05 |
| [RangerMauve/webrun-plugin-ipfs](https://github.com/RangerMauve/webrun-plugin-ipfs)| 0 | 0 | 80| 2020-03-02 | 2020-03-02 |
| [adrianleb/nextjs-daijs-example](https://github.com/adrianleb/nextjs-daijs-example)| 1 | 0 | 147| 2020-03-01 | 2020-03-05 |
| [ismailcanvardar/ipfs-smart-contract](https://github.com/ismailcanvardar/ipfs-smart-contract)| 0 | 0 | 510| 2020-02-29 | 2020-03-02 |
| [josselinchevalay/todo-ipfs](https://github.com/josselinchevalay/todo-ipfs)| 0 | 0 | 286| 2020-02-28 | 2020-02-28 |
| [KurtMerbeth/ethily](https://github.com/KurtMerbeth/ethily)| 0 | 1 | 195| 2020-02-26 | 2020-02-26 |
| [alqamahjsr/EthBazaar](https://github.com/alqamahjsr/EthBazaar)| 0 | 0 | 604| 2020-02-22 | 2020-02-22 |
| [dmerrill6/site-from-ipfs-browser-node](https://github.com/dmerrill6/site-from-ipfs-browser-node)| 0 | 0 | 266| 2020-02-21 | 2020-02-21 |
| [aquiladev/ipfs-action](https://github.com/aquiladev/ipfs-action)| 8 | 1 | 25714| 2020-02-20 | 2020-03-07 |
| [textileio/gatsby-ipfs-blog](https://github.com/textileio/gatsby-ipfs-blog)| 3 | 0 | 903| 2020-02-19 | 2020-02-22 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
