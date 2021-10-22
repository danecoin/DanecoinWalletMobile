## Danecoin Wallet

![](./img/start.png "Start Page")
![](./img/info.png "Info Page")
![](./img/seed.png "Seed Page")
![](./img/home.png "Home Page")

## Changes that need to be made
ElectumX node `wallet/wallet.ts`: electrum1.bitcoin.org

## Goals
Danecoin Wallet is a mobile wallet meant for new users to easily get started with Danecoin.

## Features
- All addresses by default are Segwit (P2WPKH-nested-in-P2SH)
- Hierarchical deterministic keys
- BIP-39 mnemonic 12 word seed
- ElectrumX backend for quick sync
- Adjust fees between 3 built-in levels
- Ability to use fiat amounts to transact

## Want to add a new feature?
The philosophy of this wallet is simplicity! Rather than adding new features, you are strongly urged to remove existing features where possible instead. When adding a new feature, you should ask yourself whether it's something which would benefit the average user of the wallet. In this way, rather than the wallet growing more complex with time, it will hopefully become more simpler.

PR's or issues discussing adding features like Multi-sig, or Lightning, or RBF, and other such things will immediately be closed. It's understandable the types of people that contribute to Danecoin software on Github are "power users", but having a wallet with a gazillion features isn't in line with the philosophy here.

## Adding or updating languages
Adding a language is simple, you need to create a new file in this directory https://github.com/danecoin/DanecoinWalletMobile/tree/main/lang with the name <language_code>.ts, for example es.ts currently contains the Spanish translations. When translating, keep in mind there are layout concerns, so try to make sure the text isn't too long, otherwise it might cause things to appear strange. This is a bigger concern in languages in which simple English words have really long equivalents.

Updating a language is as easy as updating the file with the translations in it. Some non-English translation files may have English text in some parts, this is because there may be new words or phrases added to the wallet that haven't had the chance to be translated yet. You may want to periodically look through translation files for languages you want to translate to see if any new words need to be translated.

We appreciate all translators and may from time to time reward contributions with DANE, so make sure to leave your Danecoin address in your Github profile if you're regularly making translation contributions to this project.

## Project Setup
```
yarn install
```

## Make sure rn-nodify is run
```
yarn postinstall
```

## Install pods (for iOS)
```
npx pod-install
```

## Running on iOS
```
yarn run ios
```

## Running on Android
Make sure you have Android studio set up and running either an emulator or a physical device
```
yarn run android
```

## Cleaning the project
You may need to sometimes clean the project if something goes wrong:
```
yarn clean
```
