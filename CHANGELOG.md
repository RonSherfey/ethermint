<!--
Guiding Principles:

Changelogs are for humans, not machines.
There should be an entry for every single version.
The same types of changes should be grouped.
Versions and sections should be linkable.
The latest version comes first.
The release date of each version is displayed.
Mention whether you follow Semantic Versioning.

Usage:

Change log entries are to be added to the Unreleased section under the
appropriate stanza (see below). Each entry should ideally include a tag and
the Github issue reference in the following format:

* (<tag>) \#<issue-number> message

The issue numbers will later be link-ified during the release process so you do
not have to worry about including a link manually, but you can if you wish.

Types of changes (Stanzas):

"Features" for new features.
"Improvements" for changes in existing functionality.
"Deprecated" for soon-to-be removed features.
"Bug Fixes" for any bug fixes.
"Client Breaking" for breaking CLI commands and REST routes used by end-users.
"API Breaking" for breaking exported APIs used by developers building on SDK.
"State Machine Breaking" for any changes that result in a different AppState given same genesisState and txList.

Ref: https://keepachangelog.com/en/1.0.0/
-->

# Changelog

## [Unreleased]

### Improvements

* (sdk) [\#171](https://github.com/ChainSafe/ethermint/issues/177) Bump Cosmos SDK version to [v0.38.1](https://github.com/cosmos/cosmos-sdk/releases/tag/v0.38.1)
  * Add `x/evidence` module to ethermint app
* (`x/evm`) [\#181](https://github.com/ChainSafe/ethermint/issues/181) Updated EVM module to the recommended module structure. [@fedekunze](https://github.com/fedekunze)
* (app) [\#188](https://github.com/ChainSafe/ethermint/issues/186)  Misc cleanup [@fedekunze](https://github.com/fedekunze):
  * (`x/evm`) Rename `EthereumTxMsg` --> `MsgEthereumTx` and `EmintMsg` --> `MsgEthermint` for consistency with SDK standards
  * Updated integration and unit tests to use `EthermintApp` as testing suite
  * Use expected keeper interface for `AccountKeeper`
  * Replaced `count` type in keeper with `int`
  * Add SDK events for transactions