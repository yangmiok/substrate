Secret phrase:       slide unit truck minimum fossil sentence spawn million snack lawn sock example
  Network ID:        substrate
  Secret seed:       0x4326cb59b3dbf80a1ab22d80db99ffc85522e744dc9df35b63ca1756e8032822
  Public key (hex):  0xb45981719d057d2026cf020e3603c9fdeda135125754fdd95f4df3cc95118257
  Account ID:        0xb45981719d057d2026cf020e3603c9fdeda135125754fdd95f4df3cc95118257
  Public key (SS58): 5G9B4jNUnnQFtC2YKJDPhaqHwfYorn6TrgpTGSdxWD6QryEK
  SS58 Address:      5G9B4jNUnnQFtC2YKJDPhaqHwfYorn6TrgpTGSdxWD6QryEK

  ./target/release/node-template key inspect --password-interactive --scheme Ed25519 "slide unit truck minimum fossil sentence spawn million snack lawn sock example"

Secret phrase:       slide unit truck minimum fossil sentence spawn million snack lawn sock example
  Network ID:        substrate
  Secret seed:       0x4326cb59b3dbf80a1ab22d80db99ffc85522e744dc9df35b63ca1756e8032822
  Public key (hex):  0xefe2347980aee405a6d8953b784f164cb7571171dfb92c70059df4e630d6ed20
  Account ID:        0xefe2347980aee405a6d8953b784f164cb7571171dfb92c70059df4e630d6ed20
  Public key (SS58): 5HVEVsGnhsKFeYspqW7xg9QnQSV5EDfV9ECU3J6TVeE5mk7j
  SS58 Address:      5HVEVsGnhsKFeYspqW7xg9QnQSV5EDfV9ECU3J6TVeE5mk7j



  Key password: 
Secret phrase:       jump pact since leg fold hockey scrap myself energy join sugar couple
  Network ID:        substrate
  Secret seed:       0x458715a74b7478ec63092c72aed3c993a91ddeb39c274b30937143958720d425
  Public key (hex):  0x8a4187b4e43758264cff7b36b93d993b5be8f7c558764001696088d596b47b16
  Account ID:        0x8a4187b4e43758264cff7b36b93d993b5be8f7c558764001696088d596b47b16
  Public key (SS58): 5FByvzgYy6Ahf6hx5XZpooq3n3EAv3FLL8FyAezjvdfSZwJY
  SS58 Address:      5FByvzgYy6Ahf6hx5XZpooq3n3EAv3FLL8FyAezjvdfSZwJY

  ./target/release/node-template key inspect --password-interactive --scheme Ed25519 "jump pact since leg fold hockey scrap myself energy join sugar couple"


Secret phrase:       jump pact since leg fold hockey scrap myself energy join sugar couple
  Network ID:        substrate
  Secret seed:       0x458715a74b7478ec63092c72aed3c993a91ddeb39c274b30937143958720d425
  Public key (hex):  0x7b44409d05ea3a7d6246447eee6d48b06b415a60e5ab802dfb2130ecf346aaa1
  Account ID:        0x7b44409d05ea3a7d6246447eee6d48b06b415a60e5ab802dfb2130ecf346aaa1
  Public key (SS58): 5ErL2ErQCX6y96Kks28DP6mZBQMz7ZapbrCtqhfpw7jB8KVp
  SS58 Address:      5ErL2ErQCX6y96Kks28DP6mZBQMz7ZapbrCtqhfpw7jB8KVp


# purge chain (only required for new/modified dev chain spec)
./target/release/node-template purge-chain --base-path /tmp/node01 --chain local -y

./target/release/node-template \
  --base-path /tmp/node01 \
  --chain ./customSpecRaw.json \
  --port 30333 \
  --ws-port 9945 \
  --rpc-port 9933 \
  --telemetry-url "wss://telemetry.polkadot.io/submit/ 0" \
  --validator \
  --rpc-methods Unsafe \
  --name MyNode01 \
  --password-interactive


./target/release/node-template key insert --base-path /tmp/node01 \
  --chain customSpecRaw.json \
  --scheme Sr25519 \
  --suri "slide unit truck minimum fossil sentence spawn million snack lawn sock example" \
  --password-interactive \
  --key-type aura

./target/release/node-template key insert \
  --base-path /tmp/node01 \
  --chain customSpecRaw.json \
  --scheme Ed25519 \
  --suri "slide unit truck minimum fossil sentence spawn million snack lawn sock example" \
  --password-interactive \
  --key-type gran


./target/release/node-template purge-chain --base-path /tmp/node02 --chain local -y

./target/release/node-template \
  --base-path /tmp/node02 \
  --chain ./customSpecRaw.json \
  --port 30334 \
  --ws-port 9946 \
  --rpc-port 9934 \
  --telemetry-url "wss://telemetry.polkadot.io/submit/ 0" \
  --validator \
  --rpc-methods Unsafe \
  --name MyNode02 \
  --bootnodes /ip4/34.92.224.40/tcp/30333/p2p/12D3KooWRFM1KbsNEh53RsZUzHYnCdJsno6x1RJCQbPYY8kLGbpJ \
  --password-interactive


./target/release/node-template \
  --base-path /tmp/node03 \
  --chain ./customSpecRaw.json \
  --port 30338 \
  --ws-port 9948 \
  --rpc-port 9938 \
  --telemetry-url "wss://telemetry.polkadot.io/submit/ 0" \
  --ws-external --unsafe-rpc-external \
  --rpc-methods Unsafe \
  --rpc-cors all \
  --name MyNode03 \
  --bootnodes /ip4/34.92.224.40/tcp/30333/p2p/12D3KooWRFM1KbsNEh53RsZUzHYnCdJsno6x1RJCQbPYY8kLGbpJ 


./target/release/node-template key insert --base-path /tmp/node02 \
  --chain customSpecRaw.json \
  --scheme Sr25519 \
  --suri "jump pact since leg fold hockey scrap myself energy join sugar couple" \
  --password-interactive \
  --key-type aura


./target/release/node-template key insert --base-path /tmp/node02 \
  --chain customSpecRaw.json \
  --scheme Ed25519 --suri "jump pact since leg fold hockey scrap myself energy join sugar couple" \
  --password-interactive \
  --key-type gran


docker run --rm -it --name polkadot-ui -e WS_URL=ws://35.220.173.252:9946 -p 80:80 jacogr/polkadot-js-apps:latest






# Substrate &middot; [![GitHub license](https://img.shields.io/badge/license-GPL3%2FApache2-blue)](#LICENSE) [![GitLab Status](https://gitlab.parity.io/parity/substrate/badges/master/pipeline.svg)](https://gitlab.parity.io/parity/substrate/pipelines) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](docs/CONTRIBUTING.adoc) [![Stack Exchange](https://img.shields.io/badge/Substrate-Community%20&%20Support-24CC85?logo=stackexchange)](https://substrate.stackexchange.com/)
<p align="center">
  <img src="/docs/media/sub.gif">
</p>

Substrate is a next-generation framework for blockchain innovation 🚀.

## Getting Started

Head to [docs.substrate.io](https://docs.substrate.io) and follow the [installation](https://docs.substrate.io/install/) instructions.
Then try out one of the [tutorials](https://docs.substrate.io/tutorials/).
Refer to the [Docker instructions](./docker/README.md) to quickly run Substrate, Substrate Node Template, Subkey, or to build a chain spec.

## Community & Support

Join the highly active and supportive community on the [Substrate Stack Exchange](https://substrate.stackexchange.com/) to ask questions about use and problems you run into using this software.
Please do report bugs and [issues here](https://github.com/paritytech/substrate/issues) for anything you suspect requires action in the source. 

## Contributions & Code of Conduct

Please follow the contributions guidelines as outlined in [`docs/CONTRIBUTING.adoc`](docs/CONTRIBUTING.adoc).
In all communications and contributions, this project follows the [Contributor Covenant Code of Conduct](docs/CODE_OF_CONDUCT.md).

## Security

The security policy and procedures can be found in [`docs/SECURITY.md`](docs/SECURITY.md).

## License

- Substrate Primitives (`sp-*`), Frame (`frame-*`) and the pallets (`pallets-*`), binaries (`/bin`) and all other utilities are licensed under [Apache 2.0](LICENSE-APACHE2).
- Substrate Client (`/client/*` / `sc-*`) is licensed under [GPL v3.0 with a classpath linking exception](LICENSE-GPL3).

The reason for the split-licensing is to ensure that for the vast majority of teams using Substrate to create feature-chains, then all changes can be made entirely in Apache2-licensed code, allowing teams full freedom over what and how they release and giving licensing clarity to commercial teams.

In the interests of the community, we require any deeper improvements made to Substrate's core logic (e.g. Substrate's internal consensus, crypto or database code) to be contributed back so everyone can benefit.

