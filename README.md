# 💱 IBC Cosmos Token Data


### Why this repo?

- At Pulsar we felt like there was a big gap on IBC data which prevented us from having a good way to match any IBC token to its original native token. This repo is meant to be kept updated with the current native and IBC tokens of each cosmos chain under [Cosmos Chain Registry](https://github.com/cosmos/chain-registry)
- With `ibc_data.json` you should be able to find any IBC token by its hash where the keys are in the format `ibc/HASH__CHAIN`, and using the origin property, you should be able to trace back to its original token data on `native_token_data.json`

### Known issues

- `basecro` and `uluna` have conflicts. `uluna` denom is used on [Terra, Terra2] and `basecro` on [crypto_org, cronos] chains. This has been solved in most ibcs 153 out of 162.

### Future

- Planning on adding more relevant data
- Planning on adding an API behind this data

### Hints

- The file `ibc_data.min.json` is just a minified version of `ibc_data.json`<br/>
- The file `native_token_data.min.json` is just a minified version of `native_token_data.json`<br/><br/>

#### IBC data schema:

```
{
    "ibc/HASH__CHAIN": {
        "chain": String,
        "hash": String,
        "supply": String,
        "path": String,
        "origin": {
            "denom": String,
            "chain": String | List[String] | null
        }
    }
}
```

#### Native Token data schema:

```
{
    "DENOM__CHAIN": {
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

### Useful Links

* [Website](https://pulsar.finance)
* [Discord](https://discord.gg/MEeEeyuYsU)
* [Telegram](https://t.me/pulsarfinance)
* [Twitter](https://twitter.com/Pulsarfinance)


<p align="right">(<a href="#top">back to top</a>)</p>
