---
title: API Ready Queries
description: Here you'll find a list of Queries that are ready for API use. 🪄
---

Here we have four queries, you can use the query ID from the URL in any of the [API guides](../quick-start/index.md). Or, you can fork the query and change it however you like - then use that new query ID in the API.

### Get the ERC20 balances for a given address

The query ID is [1616880](https://dune.com/queries/1616880).

| Parameters | Description | Valid Choices |
| -----------| ---------- | ---------- |
| `address` | The address that you would like to get balances for | must be a valid EVM address |
| `blocknumber` | The cutoff block for checking balances | 0 if you want most recent block, otherwise any blocknumber that has been processed will work (~3 minute/15 block delay) |
| `chain` | The EVM chain you'd like to check balances for | `ethereum`, `polygon`, `bnb`, `optimism`, `arbitrum`, `avalanche_c`, `gnosis` |
| `dust` | Keep or remove dust tokens (worth less than $0.01) | `keep` or `remove` |

Output columns

| Output Column | Description | 
| ------------- | ----------- |
| `symbol` | the token symbol, if we have it |
| `notional_value` | the notional amount of tokens held, rounded 5 decimals |
| `total_value` | the $USD value of tokens held, rounded 3 decimals |
| `token_price` | the $USD price of the token |

### Get all the holders and their balances for a given ERC20 address

The query ID is [1618116](https://dune.com/queries/1618116).

| Parameters | Description | Valid Choices |
| -----------| ---------- | ---------- |
| `address` | The ERC20 token address you would like to get holders of | must be a valid EVM address |
| `blocknumber` | The cutoff block for checking balances | 0 if you want most recent block, otherwise any blocknumber that has been processed will work (~3 minute/15 block delay) |
| `chain` | The EVM chain you'd like to check balances for | `ethereum`, `polygon`, `bnb`, `optimism`, `arbitrum`, `avalanche_c`, `gnosis` |

Output columns

| Output Column | Description | 
| ------------- | ----------- |
| `holder` | the address of the holder |
| `holder_ens` | the ens of the holder address, if any |
| `notional_value` | the notional amount of tokens held, rounded 5 decimals |
| `total_value` | the $USD value of tokens held, rounded 3 decimals |
| `token_price` | the $USD price of the token |

### Get the NFT balances for a given address

The query ID is [1617158](https://dune.com/queries/1617158).

| Parameters | Description | Valid Choices |
| -----------| ---------- | ---------- |
| `address` | The address that you would like to get balances for | must be a valid EVM address |
| `blocknumber` | The cutoff block for checking balances | 0 if you want most recent block, otherwise any blocknumber that has been processed will work (~3 minute/15 block delay) |
| `chain` | The EVM chain you'd like to check balances for | `ethereum`, `polygon`, `bnb`, `optimism`, `arbitrum`, `avalanche_c`, `gnosis` |

Output columns

| Output Column | Description | 
| ------------- | ----------- |
| `symbol` | the symbol of the NFT, if we have it |
| `name` | the name of the NFT, if we have it |
| `category`| the category of the NFT, if we have it |
| `token_id` | the token_id of the NFT |
| `contract_address` | the contract_address of the NFT |
| `acquired_how` | was it `minted` or `transfered/bought` |
| `acquired_on_block_number` | the block_number that the NFT was received on |

### Get all the holders and their balances for a given NFT address

The query ID is [1618122](https://dune.com/queries/1618122).

| Parameters | Description | Valid Choices |
| -----------| ---------- | ---------- |
| `address` | The NFT address that you would like to holders of | must be a valid EVM address |
| `blocknumber` | The cutoff block for checking balances | 0 if you want most recent block, otherwise any blocknumber that has been processed will work (~3 minute/15 block delay) |
| `chain` | The EVM chain you'd like to check balances for | `ethereum`, `polygon`, `bnb`, `optimism`, `arbitrum`, `avalanche_c`, `gnosis` |

Output columns

| Output Column | Description | 
| ------------- | ----------- |
| `holder` | the address of the holder |
| `holder_ens` | the ens of the holder address, if any |
| `tokens_held` | how many NFTs from this contract is held |
| `token_ids` | an array of all the token ids held |