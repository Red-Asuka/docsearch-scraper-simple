# Docsearch Scraper For EMQ Docs

## Install
```shell
pipenv install --keep-outdated
pipenv shell
```

## Set ENV
```shell
export APPLICATION_ID=<YOUR_APPLICATION_ID>
export API_KEY=<YOUR_API_KEY>
```

## Run
```shell
python3 -m src.index <CONFIG_FILE_NAME> <PRODUCT> <VERSION>

python3 -m src.index global-config broker v4.3
python3 -m src.index config broker v4.3
```

> `CONFIG_FILE_NAME`: `global-config` or `config`
## Links
- <https://github.com/algolia/docsearch-scraper>
- <https://github.com/Swilder-M/docsearch-scraper>


## Use for github action
```yaml
      - name: update search index
        uses: Swilder-M/docsearch-scraper-simple@v2
        env:
          APPLICATION_ID: ${{ secrets.ALGOLIA_APPLICATION_ID }}
          API_KEY: ${{ secrets.ALGOLIA_API_KEY }}
        with:
          docs_type: ${{ env.DOCS_TYPE }}
          docs_version: ${{ env.VERSION }}
```
