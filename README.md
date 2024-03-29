# wanderverse-subgraph-mainnet
Subgraph for Wanderverse contracts on mainnet.

## Generating
```sh
npx graph-compiler \
  --config source.json \
  --include node_modules/@openzeppelin/subgraphs/src/datasources \
  --export-schema \
  --export-subgraph
  ```

## Build & deploy
```sh
npx graph-cli codegen generated/oz-tokens.subgraph.yaml
npx graph-cli build generated/oz-tokens.subgraph.yaml
npx graph-cli deploy                      \
  --ipfs https://api.thegraph.com/ipfs/   \
  --node https://api.thegraph.com/deploy/ \
  username/subgraphname                   \
  generated/oz-tokens.subgraph.yaml
```
