<div align="center">
  <h1>WEB3, CRYPTOCURRENCIES and NFT resources for OSINT investigations</h1>
  <p>A curated collection of explorers, analyzers, APIs, regexes and tools for on-chain OSINT investigations.</p>
  <p>
    <img src="https://img.shields.io/badge/chains-12%2B-1f6feb" alt="Chains"/>
    <img src="https://img.shields.io/badge/updated-November%202026-2ea043" alt="Last update"/>
    <img src="https://img.shields.io/badge/license-MIT-lightgrey" alt="License: MIT"/>
    <img src="https://img.shields.io/badge/PRs-welcome-8250df" alt="PRs welcome"/>
  </p>
</div>

<p align="center"> <img src="https://github.com/user-attachments/assets/160f2000-01ac-4fbd-8e3f-100771b2ae9f" width="1000" alt="Eye"/> </p>

> [!TIP]
> **Legend:** 💰 paid / enterprise &nbsp;·&nbsp; 🔑 account or wallet login required &nbsp;·&nbsp; ⚠️ OPSEC warning: the service may log or share your queries. Use a clean browser profile, VPN and sock-puppet accounts or wallets when investigating.

## Table of contents

| Chains | Cross-chain & analytics | Web3 & tooling |
| --- | --- | --- |
| [🟠 Bitcoin](#bitcoin---btc) | [🌐 Multichain & AML analytics](#multichain--aml-analytics) | [📜 Smart contracts](#smartcontracts) |
| [🔷 Ethereum & EVM](#ethereum---eth) | [🌉 Bridges & CCTP](#bridges--cctp) | [🏦 DeFi](#defi) |
| [🔴 Tron](#tron---trx) | [🚨 Sanctions, hacks & phishing](#sanctions-hacks--phishing) | [🖼️ NFT](#nft) |
| [⚫ Monero](#monero---xmr) | [🏷️ Name services](#name-services) | [📦 IPFS](#ipfs) |
| [🔵 Cardano](#cardano---ada) | [🛡️ OPSEC](#crypto-opsec-methodologies-and-info) | [🕶️ Metaverse](#metaverse---web3) |
| [🟣 Solana](#solana---sol) | [🔎 Dorks](#dork) | [🧰 Tools](#tools) |
| [💎 TON](#toncoin---ton) | [👤 Accounts to follow](#notable-accounts-to-follow) | [🤝 Contributing](#contributing) |
| [🪙 Other chains](#other-chains) | [🕵️ Off-chain pivots](#off-chain-pivots) | [📚 Learning](#learning) |

Each chain section has the same structure: **Address Regex → Explorers → Databases and Analyzers → API → Other**.

## CRYPTO-OPSEC Methodologies and Info 
| Info / Tool | Description |
| --- | --- |
| [Slowmist Blockchain Darkforest](https://github.com/slowmist/Blockchain-dark-forest-selfguard-handbook) | Blockchain dark forest selfguard handbook: Master these, master the security of your cryptocurrency. |

<sub>[⬆ back to top](#table-of-contents)</sub>

## BITCOIN - BTC

### BTC Address Regex
| Address regex | Description |
| --- | --- |
| `1[a-km-zA-HJ-NP-Z1-9]{25,33}` | Legacy (P2PKH) addresses, 26-34 characters |
| `3[a-km-zA-HJ-NP-Z1-9]{33}` | P2SH addresses, 34 characters |
| `bc1q[qpzry9x8gf2tvdw0s3jn54khce6mua7l]{38}([qpzry9x8gf2tvdw0s3jn54khce6mua7l]{20})?` | Segwit v0 addresses (P2WPKH 42 / P2WSH 62 characters) |
| `bc1p[qpzry9x8gf2tvdw0s3jn54khce6mua7l]{58}` | Taproot addresses, 62 characters |

### BTC Blockchain explorers
| Link | Description |
| --- | --- |
| [3xpl.com](https://3xpl.com/bitcoin) | Fastest ad-free universal block explorer |
| [Blockchain.com](https://www.blockchain.com/explorer/assets/btc) | One of the first and most robust explorers, it lets you explore Bitcoin, Ethereum, Bitcoin Cash, other assets and also NFTs |
| [Blockchair](https://blockchair.com/bitcoin) | An explorer that supports different cryptocurrencies (Bitcoin, Ethereum, Dogecoin...), the search lets you query addresses, transactions and text embedded inside blocks |
| [Crystal Lite](https://lite.crystalintelligence.com/) | The public explorer of Crystal Intelligence (formerly Crystal Blockchain), search addresses and transactions and get a comprehensive overview of an address |
| [Tokenview](https://tokenview.io/) | Another blockchain explorer, it supports different tokens and cryptocurrencies, BTC, ETH, XMR... Search info by addresses and/or transactions |
| [GraphSense](https://graphsense.org/) | GraphSense is a cryptoasset analytics platform emphasizing full data sovereignty, algorithmic transparency, and scalability |
| [Coincodex](https://coincodex.com/crypto/bitcoin/historical-data/) | Historical price of Bitcoin |
| [Awebanalysis](https://awebanalysis.com/en/bitcoin-address-validate/) | Validate Bitcoin address format |
| [WalletExplorer](https://www.walletexplorer.com/) ⚠️ | A service which tries to retrieve the wallet related to an address [#BeCarefulWhatYouOSINTWith](https://www.theblock.co/linked/118223/chainalysis-used-an-ip-scraping-block-explorer-to-aid-law-enforcement-leaked-docs-say) |
| [Breadcrumbs.app](https://www.breadcrumbs.app/) 🔑 | An investigation tool that helps to visualize address relations, it also contains information about sanctioned addresses and assets. It supports BTC, ETH and any ERC-20 token |
| [TRM](https://www.trmlabs.com/) 💰 | TRM Transaction Monitoring and TRM Forensics are two tools that help with in-depth analysis of blockchain transactions |
| [Lampyre](https://lampyre.io/) ⚠️ | Like Maltego, it supports BTC investigations and correlations. [#BeCarefulWhatYouOSINTWith](https://web.archive.org/web/2020/https://keyfindings.blog/2020/03/23/be-careful-what-you-osint-with/) |
| [Bitquery.io](https://www.bitquery.io/) | Full explorer which supports address analysis, smart contracts and assets |
| [Whalealert](https://whale-alert.io/) | An alerting system, helpful to get alerts when wallets with a big amount of funds make transactions |
| [BTCparser](https://btcparser.com/) | A project to get information about different kinds of wallets, it monitors old wallets or wallets related to the Satoshi era |
| [Bitref](https://bitref.com) | A simple address explorer. It displays the amount of Bitcoin held on given addresses |
| [Arkham Intelligence](https://platform.arkhamintelligence.com) 🔑 | Entity labelling and network mapping across different chains (BTC, ETH, TRON, SOL and more) |
| [Metasleuth](https://metasleuth.io/) | BTC address explorer and wallet monitor |
| [SpyderLab](https://www.spyderlab.org/) | Spyderlab.org offers blockchain forensics, crypto AML solutions, and OSINT tools for comprehensive investigative analysis |
| [Blockstream.info](https://blockstream.info/) | Lightweight, no-JS-friendly Bitcoin and Liquid explorer by Blockstream |
| [Mempool Space](https://mempool.space/) | A graphical dashboard to analyze the history of block congestion, fees, Lightning Network and mining activities |

### BTC Blockchain Databases and Analyzers
| Link | Description |
| --- | --- |
| [Bitcoinwho'swho](https://www.bitcoinwhoswho.com/) | An address lookup service to identify reports related to malicious BTC addresses |
| [Bitcoinabuse](https://www.bitcoinabuse.com/) | Tracking bitcoin addresses used by ransomware, blackmailers, fraudsters, etc. (the database was merged into Chainabuse) |
| [Chainabuse](https://www.chainabuse.com/) | Report a cryptocurrency hack or scam across multiple blockchains and search addresses and domains to see if they are connected to any fraudulent activity. It supports BTC, ETH, TRON, SOL, ADA and more |
| [Scamsearch](https://www.scamsearch.io/) | A global scam database. Search by profile picture, email, username, pseudonym, phone number, crypto address or website |
| [Scamalert](https://scam-alert.io/) | A search engine for scams and fraud-related crypto addresses |
| [Cryptoscamdb](https://cryptoscamdb.org/scams) | A scam database which contains information about scam sites and related addresses |
| [Ransomwhere](https://ransomwhe.re/) | Bitcoin addresses used in ransomware activities, the database is in raw format and it's integrated into the Chainabuse service |
| [SPLcenter Addresslist](https://www.splcenter.org/cryptocurrency-report) | A spreadsheet containing information about addresses used by extremists and far-right communities |

### BTC API
| Req | Description |  
| --- | --- |  
| `https://3xpl.com/bitcoin/address/xxx` | Request the status of an address using 3xpl |
| `https://blockchair.com/bitcoin/address/xxx` | Request the status of an address using Blockchair |  
| `https://blockchair.com/bitcoin/transaction/xxx` | Request the details of a given transaction |  
| `https://mempool.space/api/address/xxx/txs` | Retrieve the transaction history of a given address (mempool.space REST API) |
| `https://blockchain.info/q/24hrprice` | Retrieve the price of the last 24h |  
| `https://blockchain.info/q/getreceivedbyaddress/xxx` | Retrieve the amount received by a given BTC address |  
| `https://blockchain.info/q/getsentbyaddress/xxx` | Retrieve the amount sent by a given address |  
| `https://blockchain.info/q/addressbalance/xxx` | Retrieve the balance of a given address |  
| `https://blockchain.info/q/addressfirstseen/xxx` | Retrieve the first seen date of a given address |  

### BTC Other
| Link | Description |
| --- | --- |
| [CriminalIP](https://www.criminalip.io/asset/search?query=%22Bitcoin%22%20port:%208333) | An infrastructure scanner. It scans IPs and services, there is a section related to exposed node and miner services |
| [Intelx.io](https://intelx.io/) 🔑 | It indexes information retrieved from both closed and open sources, including IPs, emails, BTC addresses and other kinds of assets |
| [Cryptocurrencyalerting](https://cryptocurrencyalerting.com/wallet-watch.html) | Get alerts about transactions related to a given address |
| [Aware Online](https://www.aware-online.com/en/osint-tools/cryptocurrency-search-tool/) | Different tools to conduct OSINT investigations on given BTC addresses |
| [GraphSense Maltego Transform](https://github.com/INTERPOL-Innovation-Centre/GraphSense-Maltego-transform) | A Maltego transform which leverages GraphSense for crypto investigations |
| [Paxful](https://paxful.com/user/XXX) | A P2P exchange that, starting from a given nickname, lets you explore users and info related to them |
| [Bitcoin prefixes address list](https://github.com/citizen010/bitcoin-prefixes-address-list) | Lists of Bitcoin addresses grouped by prefix, handy to validate or recognize address formats |

<sub>[⬆ back to top](#table-of-contents)</sub>

## ETHEREUM - ETH

### ETH Address Regex
| Address regex | Description |
| --- | --- |
| `0x[0-9A-Fa-f]{40}` | All Ethereum (and EVM) addresses have a length of 40 hexadecimal characters and begin with "0x" |

### ETH Blockchain explorers
| Link | Description |
| --- | --- |
| [3xpl.com](https://3xpl.com/ethereum) | Fastest ad-free universal block explorer |
| [Blockchain.com](https://www.blockchain.com/explorer/assets/eth) | One of the first and most robust explorers, it lets you explore Bitcoin, Ethereum, Bitcoin Cash, other assets and also NFTs |
| [Etherscan](https://etherscan.io/) | The most reliable and complete explorer for the Ethereum ecosystem. It helps to search addresses, tokens, NFTs, smart contracts and also ENS domains |
| [Blockchair](https://blockchair.com/ethereum) | An explorer that supports different cryptocurrencies (Bitcoin, Ethereum, Dogecoin...), the search lets you query addresses, transactions and text embedded inside blocks |
| [Tokenview](https://tokenview.io/) | Another blockchain explorer, it supports different tokens and cryptocurrencies, BTC, ETH, XMR... Search info by addresses and/or transactions |
| [Blockscout](https://eth.blockscout.com/) | Open-source explorer, it covers transactions, blocks, token values, sidechains and many other EVM chains |
| [Ethtective](https://ethtective.com/) | Visualizes the Ethereum network in an interactive way, which makes exploring transfers much easier |
| [GraphSense](https://graphsense.org/) | GraphSense is a cryptoasset analytics platform emphasizing full data sovereignty, algorithmic transparency, and scalability |
| [BitQuery](https://explorer.bitquery.io/ethereum) | A blockchain explorer which supports different kinds of assets. It supports BTC, ETH, DOGE, ADA etc. |
| [Ethplorer](https://ethplorer.io/) | Track portfolios of any Ethereum address with comprehensive balance charts and transactions |
| [ENS Domains](https://app.ens.domains/) | An ENS domain explorer, mainly used to purchase this kind of asset, it also helps to find ENS domains and related information |
| [Breadcrumbs.app](https://www.breadcrumbs.app/) 🔑 | An investigation tool that helps to visualize address relations, it also contains information about sanctioned addresses and assets. It supports BTC, ETH and any ERC-20 token |
| [Arkham Intelligence](https://platform.arkhamintelligence.com) 🔑 | Entity labelling and network mapping across different chains (BTC, ETH, TRON, SOL and more) |
| [Watchers.pro](https://watchers.pro) 🔑⚠️ | Needs a MetaMask login: create a sock wallet first. A tool that provides a dashboard for clustering and inspecting DeFi and altcoin related entities |
| [Metasleuth](https://metasleuth.io/) | ETH address explorer and wallet monitor |
| [TrackEnn](https://github.com/kennbroorg/trackenn) | Traceability project in blockchain. Ethereum for now. Transactions, internals, ERC-20 transfers, contracts, internal tagging, labeling, etc. |
| [Ward Graph](https://github.com/WardAnalytics/WardGraph) | Open-source graph explorer for the ETH blockchain (the hosted wardgraph.com instance is offline) |
| [Socketscan](https://www.socketscan.io/) | EVM bridge explorer |

### EVM chains explorers
Funds rarely stay on Ethereum mainnet. The same `0x` address can be checked on every EVM chain.

| Link | Chain |
| --- | --- |
| [BscScan](https://bscscan.com/) | BNB Smart Chain |
| [PolygonScan](https://polygonscan.com/) | Polygon PoS |
| [Arbiscan](https://arbiscan.io/) | Arbitrum One |
| [Basescan](https://basescan.org/) | Base |
| [Optimism Etherscan](https://optimistic.etherscan.io/) | OP Mainnet |
| [Snowtrace](https://snowtrace.io/) | Avalanche C-Chain |
| [Blockscout](https://eth.blockscout.com/) | Open-source explorer with instances for many other EVM chains and L2s |

### ETH Blockchain Databases and Analyzers
| Link | Description |
| --- | --- |
| [Chainabuse](https://www.chainabuse.com/) | Report a cryptocurrency hack or scam across multiple blockchains and search addresses and domains to see if they are connected to any fraudulent activity. It supports BTC, ETH, TRON, SOL, ADA and more |
| [Scamsearch](https://www.scamsearch.io/) | A global scam database. Search by profile picture, email, username, pseudonym, phone number, crypto address or website |
| [Cryptoscamdb](https://cryptoscamdb.org/scams) | A scam database which contains information about scam sites and related addresses |
| [SPLcenter Addresslist](https://www.splcenter.org/cryptocurrency-report) | A spreadsheet containing information about addresses used by extremists and far-right communities |
| [Walletlabels](https://www.walletlabels.xyz/) | Search engine based on a collection of more than 7.5M labeled ETH addresses | 
| [RektRadar](https://rektradar.io/) | Ethereum scam detector: mempool monitoring, deployer-graph clustering, 80+ on-chain flags per contract, groups scams by common funder |
| [etherscan-labels](https://github.com/brianleect/etherscan-labels) | Full dump of Etherscan labels in JSON / CSV (includes the phish-hack list) |
| [RolodETH](https://github.com/verynifty/RolodETH) | Open-source Ethereum address tag database |
| [Dune](https://dune.com/browse/dashboards) 🔑 | A community-driven dashboards collection, useful for exploring ETH, tokens and NFTs | 

### ETH Other
| Link | Description |
| --- | --- |
| [Chat Blockscan](https://chat.blockscan.com/index) | A chat based on the Ethereum blockchain, useful to reach an ENS domain or address owner |
| [CriminalIP](https://www.criminalip.io/asset/search?query=%22Ethereum%22%20port:%208545) | An infrastructure scanner. It scans IPs and services, there is a section related to exposed node and miner services |
| [tx2uml](https://github.com/naddison36/tx2uml) | Ethereum transaction to UML sequence diagram generator |
| [Cryptocurrencyalerting](https://cryptocurrencyalerting.com/wallet-watch.html) | Get alerts about transactions related to a given address |
| [Aware Online](https://www.aware-online.com/en/osint-tools/cryptocurrency-search-tool/) | Different tools to conduct OSINT investigations on given ETH addresses |
| [GraphSense Maltego Transform](https://github.com/INTERPOL-Innovation-Centre/GraphSense-Maltego-transform) | A Maltego transform which leverages GraphSense for crypto investigations |
| [Etherscan Transforms for Maltego](https://www.maltego.com/transform-hub/etherscan/) | The official Etherscan transform for Maltego |
| [Demixing Tornado cash bot](https://flipsidecrypto.xyz/AMLBot/demixin-eth-for-tornadocash-JCcIiS) | Tool for demixing transactions made using Tornado Cash (updated weekly) |
| [Paxful](https://paxful.com/user/XXX) | A P2P exchange that, starting from a given nickname, lets you explore users and info related to them |
| [Cielo](https://app.cielo.finance/) | A tool for tracking and monitoring EVM wallets |
| [Swiss-Knife Explorer](https://explorer.swiss-knife.xyz/) | Decodes EVM transactions and calldata in a readable way |
| [rolod0x](https://rolod0x.io/) | Private open-source address book extension: shows your own labels for addresses on any site and chain |
| [MetaSuites](https://github.com/blocksecteam/metasuites) | BlockSec browser extension (formerly MetaDock) that adds labels, fund-flow and tx tools to explorers |

<sub>[⬆ back to top](#table-of-contents)</sub>

## TRON - TRX

### TRX Address Regex
| Address regex | Description |
| --- | --- |
| `T[1-9A-HJ-NP-Za-km-z]{33}` | Base58Check address, 34 characters starting with "T" |
| `41[0-9a-fA-F]{40}` | Hex address as returned by node APIs (the "41" prefix replaces EVM "0x") |

### TRX Blockchain explorers
| Link | Description |
| --- | --- |
| [Tronscan](https://tronscan.org/) | The main TRON explorer: accounts, TRX/TRC-20 transfers, contracts, labels and USDT activity |
| [MistTrack](https://misttrack.io/) 🔑 | SlowMist AML platform: address risk score, labels and fund-flow graphs, very strong on TRON / USDT |
| [OKLink](https://www.oklink.com/tron) | Multichain explorer with address labels and TRC-20 token transfers |
| [3xpl.com](https://3xpl.com/tron) | Fastest ad-free universal block explorer |
| [Arkham Intelligence](https://platform.arkhamintelligence.com) 🔑 | Entity labelling and network mapping, supports TRON |
| [Chainabuse](https://www.chainabuse.com/) | Scam and hack reports, supports TRON addresses |

### TRX API
| Req | Description |
| --- | --- |
| `https://api.trongrid.io/v1/accounts/xxx` | Account info (balances, permissions, creation time) via TronGrid |
| `https://api.trongrid.io/v1/accounts/xxx/transactions?limit=200` | TRX transactions of a given address (paginate with `fingerprint`) |
| `https://api.trongrid.io/v1/accounts/xxx/transactions/trc20?limit=200` | TRC-20 transfers (USDT etc.) of a given address |
| [TronGrid docs](https://developers.tron.network/reference/get-account-info-by-address) | Full API reference |

<sub>[⬆ back to top](#table-of-contents)</sub>

## MONERO - XMR

### XMR Address Regex
| Address regex | Description |
| --- | --- |
| `[48][1-9A-HJ-NP-Za-km-z]{94}` | A standard Monero address is a 95-character Base58 string starting with "4" (main) or "8" (subaddress) |
| `4[1-9A-HJ-NP-Za-km-z]{105}` | Integrated address (address + payment ID), 106 characters |

### XMR Blockchain Explorers
| Link | Description |
| --- | --- |
| [Blockchair](https://blockchair.com/monero) | Helps to inspect transactions and related hashes |
| [xmrchain.net](https://xmrchain.net/) | Open-source Onion Monero Blockchain Explorer: blocks, transactions, key images, decoding outputs with a view key |
| [Explore Monero](https://exploremonero.com/) | Monero explorer with transaction and ring member details |

### XMR Blockchain Databases and Analyzers
| Link | Description |
| --- | --- |
| ~~[Antinalysis](https://antinalysis.org/example)~~ | ~~Service maintained and hosted by activists, it uses machine learning to analyze information about an address and its related transactions~~ Offline. [#BeCarefulWhatYouOSINTWith](https://www.justice.gov/opa/pr/incognito-market-owner-arrested-operating-one-largest-illegal-narcotics-marketplaces) |

<sub>[⬆ back to top](#table-of-contents)</sub>

## CARDANO - ADA

### ADA Address Regex
| Address regex | Description |
| --- | --- |
| `Ae2[1-9A-HJ-NP-Za-km-z]+` | Legacy address (Byron) - Icarus-style |
| `DdzFF[1-9A-HJ-NP-Za-km-z]+` | Legacy address (Byron) - Daedalus-style |
| `addr1[02-9ac-hj-np-z]+` | Shelley address |
| `stake1[02-9ac-hj-np-z]+` | Shelley stake (reward) address used for staking |

### ADA Blockchain explorers
| Link | Description |
| --- | --- |
| [Blockchain.com](https://www.blockchain.com/explorer/assets/ada) | One of the first and most robust explorers, it lets you explore Bitcoin, Ethereum, Bitcoin Cash, other assets and also NFTs |
| [Cardano explorer](https://explorer.cardano.org/en) | The official explorer for Cardano, it helps to analyze addresses and transactions for each epoch |
| [Blockchair](https://blockchair.com/cardano) | An explorer that supports different cryptocurrencies (Bitcoin, Ethereum, Dogecoin...), the search lets you query addresses, transactions and text embedded inside blocks |
| [Adastat](https://adastat.net/) | An explorer for the whole Cardano ecosystem, it can inspect addresses, blocks, transactions and epochs |
| [Cexplorer](https://cexplorer.io/pool) | Cardano explorer (formerly ADApools), browse stake pools and their current activities |
| [BitQuery](https://www.bitquery.io/) | Full explorer which supports address analysis, smart contracts and assets |

### ADA Blockchain Databases and Analyzers
| Link | Description |
| --- | --- |
| [Chainabuse](https://www.chainabuse.com/) | Report a cryptocurrency hack or scam across multiple blockchains and search addresses and domains to see if they are connected to any fraudulent activity. It supports BTC, ETH, TRON, SOL, ADA and more |

<sub>[⬆ back to top](#table-of-contents)</sub>

## SOLANA - SOL

### SOL Address Regex
| Address regex | Description |
| --- | --- |
| `[1-9A-HJ-NP-Za-km-z]{32,44}` | A Solana address is a Base58 string of 32 to 44 characters |

### SOL Blockchain explorers
| Link | Description |
| --- | --- |
| [Solana Explorer](https://explorer.solana.com/) | The official explorer for Solana, it helps to analyze addresses, transactions and tokens |
| [Blockchair](https://blockchair.com/solana) | An explorer that supports different cryptocurrencies (Bitcoin, Ethereum, Dogecoin...), the search lets you query addresses, transactions and text embedded inside blocks |
| [SolanaFM](https://solana.fm/) | Solana explorer with human-readable transaction decoding and labels |
| [Solscan.io](https://solscan.io/) | A Solana explorer which supports addresses, transactions, tokens and NFTs. Solscan was acquired by Etherscan |

### SOL Blockchain Databases and Analyzers
| Link | Description |
| --- | --- |
| [Chainabuse](https://www.chainabuse.com/) | Report a cryptocurrency hack or scam across multiple blockchains and search addresses and domains to see if they are connected to any fraudulent activity. It supports BTC, ETH, TRON, SOL, ADA and more |

<sub>[⬆ back to top](#table-of-contents)</sub>

## TONCOIN - TON

### TON Address Regex
| Address regex | Description |
| --- | --- |
| `-?[0-9]:[a-fA-F0-9]{64}` | The raw address: workchain id and a 64-character hex account id |
| `[EUkf0]Q[A-Za-z0-9_-]{46}` | User-friendly address (base64url with crc16 checksum): `EQ` bounceable, `UQ` non-bounceable, `kQ`/`0Q` testnet. Some insight on different kinds of [wallets](https://docs.ton.org/participate/wallets/contracts) |
| `\w+ \w+ \w+` | Some explorers also show generated nicknames like `Graceful Tan Takin` |

### TON Blockchain explorers
| Link | Description |
| --- | --- |
| [3xpl.com](https://3xpl.com/ton) | Fastest ad-free universal block explorer |
| [Tonviewer](https://tonviewer.com/) | Explorer by the Tonkeeper team, readable traces of transactions, jettons, NFTs and DNS |
| [Tonscan](https://tonscan.org/) | An address lookup service, it helps to find details about a given address |
| [Ton.sh](https://ton.sh) | An address lookup service, it helps to find details about a given address, it supports an API |
| [Toncoin](https://explorer.toncoin.org/) | A more technical explorer, it helps to query the TON network using different key fields, workchain, shard and so on |
| [TonAPI](https://docs.tonconsole.com/tonapi) | A platform and API useful to inspect TON addresses and any related assets, it supports anonymous numbers and NFTs |
| [GetGems](https://getgems.io/top-collections/) | An NFT marketplace for TON network assets |

### TON Blockchain Databases and Analyzers
| Link | Description |
| --- | --- |
| [Tonkeeper ton-assets](https://github.com/tonkeeper/ton-assets) | Community-maintained list of known TON accounts, jettons and collections |

### TON Other
| Link | Description |
| --- | --- |
| [Fragment](https://fragment.com/numbers) | A marketplace/auction used to purchase numbers or usernames usable on Telegram `https://fragment.com/username/[username]` |
| [Ton place](https://ton.place/) | A platform to monetize content and fanbase, dork `site:ton.place [content]` |
| [Tonex](https://tonex.app/) | A social network directly integrated with the TON network |
| [TONwhale](https://tonwhales.com/explorer/top) | A list of the top 1000 accounts |
| [ATOP](https://github.com/aaarghhh/a_TON_of_privacy) | A tool for investigations on TON NFTs like Telegram anonymous numbers, Telegram usernames, and TON domains |
| [TON Forbes](https://tonforbes.com) | TON Forbes is an intelligent social rating of The Open Network blockchain wallets |

### TON APIs
The v1 endpoints of tonapi.io are no longer supported, the examples below use v2.

| Link | Description |
| --- | --- |
| Get bulk info about some addresses | ```curl -X POST 'https://tonapi.io/v2/accounts/_bulk' -H 'Content-Type: application/json' -d '{"account_ids":["0:da6b1b6663a0e4d18cc8574ccd9db5296e367dd9324706f3bbd9eb1cd2caf0bf"]}'``` |
| Search for a TON domain | ```curl 'https://tonapi.io/v2/accounts/search?name=wallet.ton'``` |
| Get domain info (owner NFT, expiration) | ```curl 'https://tonapi.io/v2/dns/wallet.ton'``` |
| List Telegram anonymous numbers (collection items) | ```curl 'https://tonapi.io/v2/nfts/collections/0:0e41dc1dc3c9067ed24248580e12b3359818d83dee0304fabcf80845eafafdb2/items?limit=1000&offset=0'``` |
| Get a backresolve of a domain | ```curl 'https://tonapi.io/v2/accounts/0:ba60bfbd527c0cd2d70c6396630c50a498af015b987adaad1d4a9e287f604536/dns/backresolve'``` |
| Get current bids for a domain | ```curl 'https://tonapi.io/v2/dns/wallet.ton/bids'``` |

<sub>[⬆ back to top](#table-of-contents)</sub>

## OTHER CHAINS
| Link | Chain | Description |
| --- | --- | --- |
| [XRPScan](https://xrpscan.com/) | XRP Ledger | Accounts, payments, tokens and well-known account names |
| [Bithomp](https://bithomp.com/) | XRP Ledger | Explorer with usernames, destination tags and account history |
| [Mintscan](https://www.mintscan.io/) | Cosmos ecosystem | Explorer for Cosmos Hub and most IBC chains |
| [Subscan](https://polkadot.subscan.io/) | Polkadot | Explorer for Polkadot, with instances for Kusama and parachains |
| [Litecoin Space](https://litecoinspace.org/) | Litecoin | mempool.space-style explorer for Litecoin |
| [Blockchair](https://blockchair.com/) | Many | Also covers Dogecoin, Bitcoin Cash, Litecoin, Zcash, Dash and others |

<sub>[⬆ back to top](#table-of-contents)</sub>

## MULTICHAIN & AML ANALYTICS
| Link | Description |
| --- | --- |
| [Arkham Intelligence](https://platform.arkhamintelligence.com) 🔑 | Entity labelling, fund-flow visualizer and alerts across BTC, EVM chains, TRON, SOL and more |
| [MistTrack](https://misttrack.io/) 🔑 | SlowMist AML platform: risk scoring, labels (exchanges, mixers, hackers) and fund-flow graphs |
| [Nansen](https://www.nansen.ai/) 💰🔑 | Large wallet label database ("Smart Money", funds, exchanges) for EVM chains and Solana |
| [Metasleuth](https://metasleuth.io/) | BlockSec fund-flow tracing across BTC, EVM chains and TRON |
| [Breadcrumbs.app](https://www.breadcrumbs.app/) 🔑 | Investigation graphs with sanctioned address data |
| [Crystal Lite](https://lite.crystalintelligence.com/) | Free tier of Crystal Intelligence |
| [TRM](https://www.trmlabs.com/) 💰 | Enterprise blockchain intelligence and forensics |
| [OKLink](https://www.oklink.com/) | Multichain explorer with address labels |
| [3xpl.com](https://3xpl.com/) | Universal explorer for 40+ chains with a common API |
| [Bluepages](https://bluepages.fyi/) | Links social accounts (X / Farcaster) to crypto addresses and back, great for pivoting from an address to a persona |
| [OnChainRisk](https://onchainrisk.io/) | Multichain wallet analysis, risk scoring and fund-flow tracing |
| [AMLBot](https://amlbot.com/) 💰 | AML address checks and investigation service, popular for TRON / USDT |
| [Scorechain](https://www.scorechain.com/) 💰 | Blockchain analytics and AML risk scoring for compliance teams |
| [Elliptic](https://www.elliptic.co/) 💰 | Enterprise blockchain analytics and investigations (Elliptic Investigator) |
| [Chainalysis Reactor](https://reactor.chainalysis.com/) 💰🔑 | Chainalysis investigation software used by law enforcement |
| [Bubblemaps](https://bubblemaps.io/) | Visualizes token holder clusters, useful to spot insiders and related wallets behind a token |

<sub>[⬆ back to top](#table-of-contents)</sub>

## BRIDGES & CCTP
| Link | Description |
| --- | --- |
| [Range](https://explorer.range.org/) | CCTP (Circle USDC) transactions explorer |
| [Wormholescan](https://wormholescan.io/) | Wormhole bridge transfers and messages explorer |
| [LayerZero Scan](https://layerzeroscan.com/) | LayerZero cross-chain messages explorer (Stargate and other OFT bridges) |
| [Socketscan](https://www.socketscan.io/) | Explorer for bridges aggregated by Socket / Bungee |

<sub>[⬆ back to top](#table-of-contents)</sub>

## SANCTIONS, HACKS & PHISHING
| Link | Description |
| --- | --- |
| [OFAC Sanctions List Search](https://sanctionssearch.ofac.treas.gov/) | Official US Treasury SDN search, includes listed crypto addresses |
| [OpenSanctions](https://www.opensanctions.org/) | Open database of sanctioned entities and PEPs, includes crypto wallet identifiers |
| [SlowMist Hacked](https://hacked.slowmist.io/) | Database of blockchain hacks and incidents with dates, amounts and attack types |
| [Rekt Leaderboard](https://rekt.news/leaderboard/) | Biggest DeFi exploits with post-mortems |
| [DefiLlama Hacks](https://defillama.com/hacks) | Hacks database with amounts, techniques and chains |
| [Solodit](https://solodit.xyz/) | Searchable database of audit findings and exploits |
| [ChainSec DeFi Hacks](https://www.chainsec.io/defi-hacks) | List of DeFi hacks with links to analyses |
| [BlockThreat](https://blockthreat.com/) | Weekly newsletter on hacks, scams and threat intel in crypto |
| [eth-phishing-detect](https://github.com/MetaMask/eth-phishing-detect) | MetaMask's list of known phishing domains |
| [Chainabuse](https://www.chainabuse.com/) | Community scam and hack reports for addresses and domains |

<sub>[⬆ back to top](#table-of-contents)</sub>

## NAME SERVICES
| Link | Description |
| --- | --- |
| [ENS Domains](https://app.ens.domains/) | `.eth` names: owner, resolver, records and history |
| [Unstoppable Domains](https://unstoppabledomains.com/) | `.crypto`, `.x`, `.nft` and other names, search shows linked addresses |
| [SNS](https://www.sns.id/) | Solana Name Service (`.sol`) |
| [TON DNS via TonAPI](#ton-apis) | `.ton` and `.t.me` names, see the TON API examples |

<sub>[⬆ back to top](#table-of-contents)</sub>

## OFF-CHAIN PIVOTS
Once an address is linked to a name or a company, these sources help to continue the investigation off-chain.

| Link | Description |
| --- | --- |
| [ICIJ Offshore Leaks](https://offshoreleaks.icij.org/) | Panama / Pandora / Paradise Papers entities, officers and intermediaries |
| [OCCRP Aleph](https://aleph.occrp.org/) 🔑 | Company registries, leaks and court records from OCCRP |
| [LeakIX](https://leakix.net/) | Exposed services and leaks search, useful for crypto infrastructure (nodes, wallets, panels) |
| [hunter.how](https://hunter.how/) | Internet-wide asset search engine, an alternative to Shodan / CriminalIP |

<sub>[⬆ back to top](#table-of-contents)</sub>

## SMARTCONTRACTS
| Tool | Description |
| --- | --- |
| [Phalcon Explorer](https://blocksec.com/phalcon/explorer) | BlockSec transaction explorer: invocation flow, fund flow and balance changes, great for exploit analysis |
| [Tenderly Explorer](https://dashboard.tenderly.co/explorer) 🔑 | Transaction debugger and simulator for EVM chains |
| [Ethereum Signature Database](https://www.4byte.directory/) | A database mapping 4-byte function selectors to function signatures |
| [Grep.app](https://grep.app/search?q=solidity) | Search for smart contract source code. It could be useful to search for NFT or contract source code |
| [EIS3](https://github.com/salaheldinaz/EIS3) | An ENS domain (.eth domain) analyzer |
| [heimdall-rs](https://github.com/Jon-Becker/heimdall-rs) | EVM bytecode decompiler and toolkit, works on unverified contracts |
| [whatsABI](https://github.com/shazow/whatsabi) | Recovers function selectors and ABI from unverified contract bytecode |
| [Dedaub Library](https://library.dedaub.com/) | Decompiled and verified contracts search across EVM chains |
| [Otterscan](https://github.com/otterscan/otterscan) | Fast local block explorer on top of your own Erigon / Reth node, no third party sees your queries |
| [De.Fi Scanner](https://de.fi/scanner) | Smart contract risk scanner (honeypots, owner privileges, proxy) |
| [revoke.cash](https://revoke.cash/) | Shows token approvals of an address, useful to understand drainer victims |
| [Dune](https://dune.com/browse/dashboards) 🔑 | A community-driven dashboards collection, useful for exploring ETH, tokens and NFTs | 

<sub>[⬆ back to top](#table-of-contents)</sub>

## DEFI
| Tool | Description |
| --- | --- |
| [DefiLlama](https://defillama.com/) | TVL, protocol, bridge and stablecoin analytics across chains |
| [Debank](https://debank.com/) | A WEB3 portfolio tracker and messenger |
| [Zapper](https://zapper.xyz/) | A multichain WEB3 explorer. It allows you to search and monitor different kinds of assets like tokens, NFTs etc. |

<sub>[⬆ back to top](#table-of-contents)</sub>

## NFT
| Tool | Description |
| --- | --- |
| [Opensea](https://opensea.io/) | The first and most relevant NFT marketplace, it also supports ENS names, accounts can be explored using this pattern: https://opensea.io/[nickname] |
| [Binance NFT](https://www.binance.com/en/nft/) | NFT marketplace directly managed by Binance |
| [Rarible](https://rarible.com/) | Another NFT marketplace, it supports ETH, SOL, Tezos and Polygon |
| [Crypto.com](https://crypto.com/nft) | NFT marketplace directly managed by Crypto.com |
| [NFT Calendar](https://nftcalendar.io/) | A calendar for NFT projects, it doesn't require any author validation |
| [NFTfinder](https://www.nyckel.com/nft-finder/) | A reverse search for finding NFTs, it supports images, addresses and so on | 
| [Compass](https://compass.art/pulse) | An explorer which helps to understand statistics about NFTs |
| [NFT Analyst Starter Pack](https://github.com/a16z/nft-analyst-starter-pack) | Using an Alchemy API key, it can generate CSV extracts for all token transfers, historical sales, and each underlying item's metadata |
| [GetGems](https://getgems.io/top-collections/) | Another NFT marketplace for TON network assets |
| [NFTGO.io](https://nftgo.io/) | Discover, analyze, and trade NFTs, aided by in-depth analytics and toolkits |
| [NFT scan](https://www.nftscan.com/) | An NFT explorer which supports different blockchains like Ethereum, BNB Chain, Polygon, Solana and others |
| [Dune](https://dune.com/browse/dashboards) 🔑 | A community-driven dashboards collection, useful for exploring ETH, tokens and NFTs | 
| [ZORA](https://zora.co/collect/eth:0x054460490780a6eb15625d703db1754e0b78d846) | A platform for minting NFTs, it lets you explore useful mint statistics |

### NFT Databases and Analyzers
| Link | Description |
| --- | --- |
| [Scamsniffer](https://explorer.scamsniffer.io/?sort=30DayVolume) | A full solution to track NFT scammers, it also supports a browser extension and a Discord bot |

### NFT API
| Tool | Description | API CALL |
| --- | --- | --- |
| [Alchemy API](https://www.alchemy.com/nft-api) | Helps to navigate ETH and other chain data via API | `import { Alchemy } from "alchemy-sdk";new Alchemy().nft.getNftsForOwner("0xshah.eth").then(console.log);` |

<sub>[⬆ back to top](#table-of-contents)</sub>

## IPFS
| Tool | Description |
| --- | --- |
| `ipfs routing findprovs <cid>` | Returns the IDs of all nodes having the file (formerly `ipfs dht findprovs`) |
| `ipfs routing findpeer <nodeID>` | Returns the list of node addresses (IPv4 and IPv6, TCP and UDP) (formerly `ipfs dht findpeer`) |
| [IPFS scanner](https://github.com/cryptodashie/ipfs/tree/fda709851b21d9ef82eb246da6f96667f14f3ae8) | IPFS scanning can identify newly hosted content or expose information leaks similar to Amazon S3 buckets | 
| [IPFS browser](https://ipfsbrowser.com/) | Search, view, access, and download IPFS files right in your web browser from any device |

<sub>[⬆ back to top](#table-of-contents)</sub>

## METAVERSE - WEB3
| LINK | Description |
| --- | --- |
| [Spatial](https://www.spatial.io) | An example of a Metaverse, it contains different spaces where people can connect. `https://www.spatial.io/@[USERNAME]` |
| [Scamsniffer](https://www.scamsniffer.io/extension/) | A browser extension aimed at blocking and detecting scams and rug pulls while surfing WEB3 |

<sub>[⬆ back to top](#table-of-contents)</sub>

## DORK
| Dork | Description |
| --- | --- |
| `"[ADDRESS]" -block` | Find pages mentioning the address while filtering out block explorer noise |
| `site:[url of interest] "[ADDRESS]"` | Helps to find information about an address on a target url of interest |
| `"antminer" http.title:"401"` | (Shodan) dork for exposed Antminer devices |
| `"ETH - Total Speed"` | (Shodan) Claymore Miner Software |

<sub>[⬆ back to top](#table-of-contents)</sub>

## NOTABLE ACCOUNTS TO FOLLOW
| Account | Description |
| --- | --- |
| [CIA_Officer](https://x.com/officer_cia) | Independent Security Researcher • Not the CIA • OpSec & Privacy Guru • On-Chain & OSINT Sleuth |
| [Rugpullfinder (Inactive)](https://x.com/rugpullfinder) | The NFT community's premier source of information |
| [ZachXBT](https://x.com/zachxbt) | On-chain sleuth. Rug pull survivor turned 2D detective |
| [ZachXBT investigations](https://zachxbt.mirror.xyz/) | Long-form investigations by ZachXBT on Mirror |
| [PeckShieldAlert](https://x.com/PeckShieldAlert) | Real-time alerts on hacks, exploits and stolen funds movements |
| [BlockSecTeam](https://x.com/BlockSecTeam) | Exploit analyses and attack alerts from BlockSec (Phalcon, MetaSleuth) |
| [CertiKAlert](https://x.com/CertiKAlert) | Alerts on exploits, rug pulls and phishing |
| [MistTrack_io](https://x.com/MistTrack_io) | SlowMist's AML team: fund tracing of hacks and scams |
| [Lookonchain](https://x.com/lookonchain) | Whale and fund movements tracking |

<sub>[⬆ back to top](#table-of-contents)</sub>

## TOOLS
| Tool | Description |
| --- | --- |
| [Obsidian template: crypto investigation report](https://github.com/theNerdInTheHighCastle/obsidian-osint-templates/blob/main/--%20templates/Cryptocurrency%20Investigation%20Findings%20Report.md) | An Obsidian template for cryptocurrency investigations |
| [Obsidian templates NFT](https://github.com/theNerdInTheHighCastle/obsidian-osint-templates/blob/main/--%20templates/NFT.md) | An Obsidian template for NFT investigations |
| [Eth Explorers Extension](https://github.com/apoorvlathey/eth-explorers-extension) | Browser extension to open Ethereum addresses & transaction hashes from any page on popular explorers + dashboards |
| [Maltego](https://www.maltego.com/) 💰 | Maltego directly supports BTC and ETH address entities. It is a tool used for OSINT and forensic investigations |
| [Tatum Blockchain Explorer (Maltego Transform)](https://www.maltego.com/) | Tatum is a blockchain development platform that supports over 40 blockchain protocols and 2000+ digital assets |
| [Opensanctions (Maltego Transform)](https://www.maltego.com/) | A transform for Maltego, it queries sanctioned addresses from the OpenSanctions database |
| [EMER name (Maltego Transform)](https://github.com/Tomasuh/Maltego_Transform_Blockchain_DNS/tree/63e6fb152a75893103ec038b9974db937ba21baa) | Useful transform to resolve EMER domain names |
| [Mugetsu](https://t.me/the_mugetsu_bot) | Correlation from X handles, wallet identification, trading analysis and wallet explorer |
| [Impersonator](https://chromewebstore.google.com/detail/impersonator/hgihfkmoibhccfdohjdbklmmcknjjmgl) | Spoof an ETH address for authenticating in dApps |
| [INTERPOL Hardware Wallets List](https://github.com/INTERPOL-Innovation-Centre/HardwareWallets_DF_List) | Hardware wallets catalogue with photos, to recognize devices during searches and seizures |
| [Chainlist](https://chainlist.org/) | Chain IDs and RPC endpoints for every EVM network |

<sub>[⬆ back to top](#table-of-contents)</sub>

## LEARNING
| Link | Description |
| --- | --- |
| [Basel Institute eLearning](https://learn.baselgovernance.org/) | Free courses on crypto investigations, asset recovery and AML for law enforcement and compliance |
| [On-Chain Investigations Tools List](https://github.com/OffcierCia/On-Chain-Investigations-Tools-List) | Huge link collection by officercia, several entries above come from it |

<sub>[⬆ back to top](#table-of-contents)</sub>

## CONTRIBUTING
Found a dead link or a tool that should be here? Open an issue or a pull request. Please keep one resource per row, say what it does in one sentence and mark it with 💰 / 🔑 / ⚠️ when it applies.
