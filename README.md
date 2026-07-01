# POSTHUMAN IBC Relayers

This repository is a public reference for IBC relayer addresses operated or
historically operated by POSTHUMAN.

## Current Status

The old Hermes relayer host `78.47.68.236` was retired for relayer use on
2026-06-03.

A replacement Hermes relayer is staged on `135.181.227.236`, but the
`hermes-relayer.service` unit is intentionally disabled and inactive until the
team chooses the exact chains, paths, and channels to relay.

Live verification on 2026-07-01:

- `hermes-relayer.service`: disabled
- `hermes-relayer.service`: inactive
- Hermes config validation: passed

## Staged Hermes Chains

| Chain | Chain ID | Relayer Address | Explorer |
| --- | --- | --- | --- |
| Osmosis | `osmosis-1` | `osmo15z4tpg5yxc9f0a2xuh52hj0cpyz66y95atdg86` | [Mintscan](https://www.mintscan.io/osmosis/account/osmo15z4tpg5yxc9f0a2xuh52hj0cpyz66y95atdg86) |
| Juno Network | `juno-1` | `juno1kmh5nvfrsatc3v7ssgszzrlxsdz7f3czmdu5wj` | [Mintscan](https://www.mintscan.io/juno/account/juno1kmh5nvfrsatc3v7ssgszzrlxsdz7f3czmdu5wj) |
| Cosmos Hub | `cosmoshub-4` | `cosmos1aea0vly7lklqrkxjpvch8z5dekmxqwyk8kr4px` | [Mintscan](https://www.mintscan.io/cosmos/address/cosmos1aea0vly7lklqrkxjpvch8z5dekmxqwyk8kr4px) |
| Neutron | `neutron-1` | `neutron1h3grxcfts9uc8lvu9vclhahus2npk24pw40fnd` | [Mintscan](https://www.mintscan.io/neutron/address/neutron1h3grxcfts9uc8lvu9vclhahus2npk24pw40fnd/) |

## Notes

- Injective relaying is not currently included in the staged Hermes setup.
  Hermes 1.13.2 does not support Injective `ethsecp256k1` accounts; use Hermes
  2.x or another relayer if Injective relaying is required again.
- Retired or migrated networks from the old public list, including Chihuahua,
  OmniFlix, Odin Protocol, AssetMantle, and Injective, should not be treated as
  active POSTHUMAN relayer coverage.
- Before starting the relayer, check key balances, RPC/gRPC reachability, and
  the exact channel/path scope.

## Operational Reference

Internal POSTHUMAN operators should use the local Hermes guide as the canonical
runbook:

`knowledge/validator/utils/guides/relayer.md`
