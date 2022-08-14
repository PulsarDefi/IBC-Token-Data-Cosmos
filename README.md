# IBC-Cosmos data 👮

Planning on adding more data in the future<br/><br/>
The file `ibc_data.min.json` is just a minified version of `ibc_data.json`<br/>
The file `native_token_data.min.json` is just a minified version of `native_token_data.json`<br/><br/>
IBC data schema:
```
{
    "ibc_hash": {
        "chain": String,
        "supply": String,
        "channel": String,
        "denom": String
    }
}
```
Native Token data schema:
```
{
    "denom": {
        "chain": String,
        "name": String,
        "denom": String,
        "symbol": String,
        "decimals": integer,
        "description": String,
        "coingecko_id": String | null,
        "logos": {
          String: String
        }
    },
}
```

<p align="right">(<a href="#top">back to top</a>)</p>
