# Docsearch Scraper For EMQ Docs

## Install
```shell
pipenv install --keep-outdated
pipenv shell
```

## Use
```shell
export APPLICATION_ID=<YOUR_APPLICATION_ID>
export API_KEY=<YOUR_API_KEY>
export CONFIG=$(cat config.json | jq -r tostring)

python3 -m src.index
```
