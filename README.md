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
*  7/2020: 96
*  6/2020: 67
*  5/2020: 64
*  4/2020: 65
*  3/2020: 58
*  2/2020: 58
*  1/2020: 61
*  12/2019: 56
*  11/2019: 53
*  10/2019: 65
*  9/2019: 63
*  8/2019: 71

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

Total Matches: 1740

Total Results (Limited by GitHUB API): 348

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [wabarc/wbipfs](https://github.com/wabarc/wbipfs)| 0 | 0 | 9724| 2020-07-04 | 2020-07-04 |
| [utkarsh23/access-control-for-IPFS](https://github.com/utkarsh23/access-control-for-IPFS)| 0 | 0 | 8| 2020-06-19 | 2020-06-19 |
| [StreamSpace/ss-ds-store](https://github.com/StreamSpace/ss-ds-store)| 0 | 0 | 11| 2020-06-13 | 2020-06-13 |
| [BasitAwan/IPFS-Crawler](https://github.com/BasitAwan/IPFS-Crawler)| 0 | 0 | 1675| 2020-06-10 | 2020-06-10 |
| [shiningacg/ipfs-filestore](https://github.com/shiningacg/ipfs-filestore)| 0 | 0 | 3863| 2020-06-04 | 2020-06-14 |
| [storj-thirdparty/driver-ipfs](https://github.com/storj-thirdparty/driver-ipfs)| 0 | 0 | 545| 2020-06-01 | 2020-07-02 |
| [bonedaddy/flloyd-archiver](https://github.com/bonedaddy/flloyd-archiver)| 4 | 0 | 108| 2020-05-31 | 2020-06-04 |
| [vulcanize/eth-ipfs-state-validator](https://github.com/vulcanize/eth-ipfs-state-validator)| 1 | 0 | 75| 2020-05-30 | 2020-07-01 |
| [storj-thirdparty/connector-ipfs](https://github.com/storj-thirdparty/connector-ipfs)| 0 | 1 | 220| 2020-05-30 | 2020-07-02 |
| [boomlinde/ipfs-gopher](https://github.com/boomlinde/ipfs-gopher)| 9 | 0 | 9| 2020-05-30 | 2020-05-31 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_go.md)

#### JS Repositories

Total Matches: 73486

Total Results (Limited by GitHUB API): 1329

| repo | watchers | forks | size | created | pushed |
| ---- | -------- | ----- | ---- | ------- | ------ |
| [plemonopoulos/upload_images_ipfs](https://github.com/plemonopoulos/upload_images_ipfs)| 0 | 0 | 935| 2020-07-01 | 2020-07-01 |
| [VIkash2601/eth_ipfs_file_upload](https://github.com/VIkash2601/eth_ipfs_file_upload)| 0 | 0 | 465| 2020-06-27 | 2020-07-02 |
| [rafaelramalho19/ipfs-css-icons](https://github.com/rafaelramalho19/ipfs-css-icons)| 0 | 0 | 191| 2020-06-26 | 2020-06-26 |
| [marstech3/block-doc](https://github.com/marstech3/block-doc)| 0 | 0 | 945| 2020-06-26 | 2020-07-04 |
| [Gozala/js-ipfs-lite-http-client](https://github.com/Gozala/js-ipfs-lite-http-client)| 0 | 0 | 12| 2020-06-25 | 2020-07-01 |
| [ipfs-africa/ipfs-africa.github.io](https://github.com/ipfs-africa/ipfs-africa.github.io)| 0 | 0 | 6922| 2020-06-23 | 2020-06-24 |
| [ChiranjibiRout/IPFS-Ethereum-React-Stora...](https://github.com/ChiranjibiRout/IPFS-Ethereum-React-Storage)| 0 | 0 | 229| 2020-06-21 | 2020-06-21 |
| [heEXDe/electronJS-IPFS-experiments](https://github.com/heEXDe/electronJS-IPFS-experiments)| 0 | 0 | 121| 2020-06-18 | 2020-07-04 |
| [enochzhao/ipfs-disk-test](https://github.com/enochzhao/ipfs-disk-test)| 0 | 0 | 428| 2020-06-18 | 2020-06-18 |
| [ingenium21/rart-project](https://github.com/ingenium21/rart-project)| 2 | 0 | 272| 2020-06-16 | 2020-06-23 |


The above set is limited to the 10 most recently created. 
[Full table here.](./results/repo_search_js.md)
