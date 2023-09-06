# Cobalt Pay - Accept Bitcoin Payments ₿

[![GitHub tag](https://img.shields.io/badge/dynamic/json.svg?url=https://raw.githubusercontent.com/CobaltApp/CobaltPay/master/package.json&query=$.version&label=Version)](https://github.com/CobaltApp/CobaltPay)
![](https://img.shields.io/github/license/CobaltApp/CobaltPay)

Cobalt Pay is an open-source Bitcoin payment processor, built from BTC Pay Server, which allows you to accept bitcoin without any intermediaries.

## 🌟 Features

* Direct, peer-to-peer Bitcoin payments
* No transaction fees (other than the [network fee](https://en.bitcoin.it/wiki/Miner_fees))
* No fees, middleman or KYC
* Non-custodial (complete control over the private key)
* Enhanced privacy & security
* Self-hosted
* SegWit support
* Lightning Network support (LND, Core Lightning (CLN), Eclair)
* Tor support
* Share your instance with friends (multi-tenant)
* Invoice management and Payment requests
* Apps: Point of sale, crowdfunding, donation button
* Full-node reliant wallet with [hardware wallet integration](https://docs.btcpayserver.org/Vault/) and SegWit support
* Bitcoin-only build, separate community-maintained altcoin build ([supported altcoins](https://docs.btcpayserver.org/FAQ/FAQ-Altcoin/))

## 🚀 Getting Started

Firstly, decide if you want to host an instance yourself or use a [third-party host](https://docs.btcpayserver.org/ThirdPartyHosting/). If you've chosen to self-host, there are plenty of documented [ways to deploy Cobalt Pay](https://docs.btcpayserver.org/Deployment/).

After successful deployment, make sure to check our [getting started](https://docs.btcpayserver.org/RegisterAccount/) and [walkthrough](https://docs.btcpayserver.org/Walkthrough/) guides. In case you would like to use Lightning Network, see [Lightning guide](https://docs.btcpayserver.org/LightningNetwork/).

## 📚 Documentation

Please check out our [official website](https://btcpayserver.org/), [complete documentation](https://docs.btcpayserver.org/) and [FAQ](https://docs.btcpayserver.org/FAQ/) for more details.

If you have trouble using BTCPay Server, consider joining [communities listed on the official website](https://btcpayserver.org/#communityCTA) to get help from other contributors. Only create a [GitHub issue](https://github.com/btcpayserver/btcpayserver/issues/new/choose) for technical issues you can't resolve through other channels or feature requests you've validated with other members of the community.

## 🧑‍💻 Developing

To begin developing locally, visit our [local development guide](https://docs.btcpayserver.org/Development/LocalDevelopment/). There are also several video-tutorials:

* [Setting up development environment on Windows](https://www.youtube.com/watch?v=ZePbMPSIvHM)
* [Setting up development environment Linux (Ubuntu)](https://www.youtube.com/watch?v=j486T_Rk-yw&t)
* [Setting up development environment MacOS](https://www.youtube.com/watch?v=GWR_CcMsEV0)

### How to build

While the documentation advises using docker-compose, you may want to build Cobalt Pay yourself.

First, install .NET Core SDK v6.0 as specified by the [Microsoft website](https://dotnet.microsoft.com/download/dotnet-core/6.0).

On Powershell:

```powershell
.\build.ps1
```

On linux:

```sh
./build.sh
```

### How to run

Use the `run` scripts to run Cobalt Pay, this example shows how to print the available command-line arguments of Cobalt Pay.

On Powershell:

```powershell
.\run.ps1 --help
```

On linux:

```sh
./run.sh --help
```

### How to debug

If you want to debug, use Jetbrain's Rider or Visual Studio 2022.

You need to run the development time docker-compose as described [in the test guide](./BTCPayServer.Tests/README.md).

You can then run the debugger by using the Launch Profile `Docker-Regtest`.

If you need to debug ledger wallet interaction, install the development time certificate with:

```bash
# Install development time certificate in the trust store
dotnet dev-certs https --trust
```

Then use the `Docker-Regtest-https` debug profile.

### Other dependencies

For more information, see the documentation:
[How to deploy a Cobalt Pay instance](https://docs.btcpayserver.org/Deployment/).

## 🤝 Community

Our community is the 💙 of the project. To chat with other community members in real-time, join our [Telegram channel](https://t.me/cobaltapp).

## 📜 License

Cobalt Pay software is provided under the [MIT License](https://github.com/CobaltApp/CobaltPay/blob/master/LICENSE).

## ❓ FAQ

Report a bug [here](https://github.com/CobaltApp/CobaltPay/issues/new/choose)
Builds automated and tested with [BrowserStack](https://www.browserstack.com)
Bugs reported via [BugSnag](https://www.bugsnag.com)
If you'd like to support the project, please visit the [donation page](https://cobalt-pay.com/donate/).
