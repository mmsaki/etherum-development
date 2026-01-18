# JSON-RPC

In order for any application to interact with Ethereum blockchain (i.e read blockchain data, or send transactions) it must connect to a an Ethereum node.

Every ethereum client implements the JSON-RPC spec, so there is a uniform set of methods that all apps can rely on.

## Assignmemt

1. Find all the JSON_RPC methods api to interact with ethereum clients.
1. Demontrate that how you can read and send data to the ethereum blockchain through json-rpc.

## Submissions

1. Submit a github repository with all the JSON-RPC methods for etheruem clients and document how to use those methods.

## Places where JSON-RPC is shown

### Geth `geth --http`

- [getting started (geth)](https://geth.ethereum.org/docs/getting-started)

```sh
curl -X POST http://127.0.0.1:8545 \ -H "Content-Type: application/json" \
  --data '{"jsonrpc":"2.0", "method":"eth_getBalance", "params":["0xca57f3b40b42fcce3c37b8d18adbca5260ca72ec","latest"], "id":1}'
```

or

```sh
geth attach http://127.0.0.1:8545
```

```sh
> eth.gasPrice
```

### Foundry: forge, cast, anvil

- [interact with json-rpc](https://getfoundry.sh/introduction/getting-started#interact-with-json-rpc)
- [anvil supported rpc methods](https://getfoundry.sh/anvil/reference/)

```sh
cast block-number --rpc-url https://reth-ethereum.ithaca.xyz/rpc
# forks
forge test --fork-url https://reth-ethereum.ithaca.xyz/rpc
# forge create
forge script script/Counter.s.sol:CounterScript \
--rpc-url $RPC_URL
```

### Browser wallet: metamask

```js
const [address] = await window.ethereum.request({ 
  method: 'eth_requestAccounts' 
})
```

### Web3 libraries: Viem, Web3js, Web3py

-

### Tenderly

- [tenderly_* namespace]()

```ts
const simulation = await client.request({
  method: "tenderly_simulateTransaction",
  params: [
    // transaction object
    {
      from: "0xd8da6bf26964af9d7eed9e03e53415d37aa96045",
      to: "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      gas: "0x0",
      gasPrice: "0x0",
      value: "0x0",
      data: "0xa9059cbb00000000000000000000000020a5814b73ef3537c6e099a0d45c798f4bd6e1d60000000000000000000000000000000000000000000000000000000000000001",
    },
    // the block
    "latest",
  ],
});
 
console.log("Trace");
console.log(JSON.stringify(simulation.trace, null, 2));
console.log("=======================================================");
console.log("Logs");
console.log(JSON.stringify(simulation.logs, null, 2));
console.log("=======================================================");
console.log("Asset Changes");
console.log(JSON.stringify(simulation.assetChanges, null, 2));
console.log("=======================================================");
console.log("Balance Changes");
console.log(JSON.stringify(simulation.balanceChanges, null, 2));
```
