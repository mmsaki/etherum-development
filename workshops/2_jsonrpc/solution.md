## Block methods

- [eth/block.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/block.yaml)

## eth_getBlockByHash

Returns information about a block by hash.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByHash",
  "params": [
    "0xd5f1812548be429cbdc6376b29611fc49e06f1359758c4ceaaa3b393e2239f9c",
    false
  ]
}
```

gets block 1

```sh
>> {"jsonrpc":"2.0","id":1,"method":"eth_getBlockByHash","params":["0x79ba0368c2c6563a7d263695b583dcc6d1c25d4988daa0105804d38bdd987f2f",true]}
<< {"jsonrpc":"2.0","id":1,"result":{ ... }}
```

gets block empty hash

```
>> {"jsonrpc":"2.0","id":1,"method":"eth_getBlockByHash","params":["0x0000000000000000000000000000000000000000000000000000000000000000",true]}
<< {"jsonrpc":"2.0","id":1,"result":null}
```

## eth_getBlockByNumber

Returns information about a block by number.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByNumber",
  "params": [
    "0x68b3",
    false
  ]
}
```

## eth_getBlockTransactionCountByHash

Returns the number of transactions in a block from a block matching the given block hash.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByHash",
  "params": [
    "0xb903239f8543d04b5dc1ba6579132b143087c68db1b2168786408fcbce568238"
  ]
}
```

## eth_getBlockTransactionCountByNumber

Returns the number of transactions in a block matching the given block number.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByNumber",
  "params": [
    "0xe8"
  ]
}
```

## eth_getUncleCountByBlockHash

Returns the number of uncles in a block from a block matching the given block hash.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockHash",
  "params": [
    "0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35"
  ]
}
```

## eth_getUncleCountByBlockNumber

Returns the number of transactions in a block matching the given block number.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockNumber",
  "params": [
    "0xe8"
  ]
}
```

## eth_getBlockReceipts

Returns the receipts of a block by number or hash.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockReceipts",
  "params": [
    "latest"
  ]
}
```

## Client methods

- [eth/client.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/client.yaml)

## eth_accounts

Returns list of accounts owned by client.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_accounts",
  "params": []
}
```

## eth_blobBaseFee

Returns the base fee per blob gas fee in wei.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_blobBaseFee",
  "params": []
}
```

## eth_chainId

Returns the chain ID of the current network.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_chainId",
  "params": []
}
```

## eth_syncing

Returns an object with data about the sync status or false.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_syncing",
  "params": []
}
```

## eth_coinbase

Returns the client coinbase address.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_coinbase",
  "params": []
}
```

## eth_blockNumber

Returns the number of most recent block.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_blockNumber",
  "params": []
}
```

## Execute methods

- [eth/execute.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/execute.yaml)

## eth_call

Executes a new message call immediately without creating a transaction on the block chain.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_call",
  "params": [
    {
      "to": "0x69498dd54bd25aa0c886cf1f8b8ae0856d55ff13",
      "value": "0x1"
    },
    "latest"
  ]
}
```

## eth_estimateGas

Generates and returns an estimate of how much gas is necessary to allow the transaction to complete.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_estimateGas",
  "params": [
    {
      "from": "0xfe3b557e8fb62b89f4916b721be55ceb828dbd73",
      "to": "0x44aa93095d6749a706051658b970b941c72c1d53",
      "value": "0x1"
    }
  ]
}
```

## eth_createAccessList

Generates an access list for a transaction.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_createAccessList",
  "params": [
    {
      "from": "0xaea8f8f781326bfe6a7683c2bd48dd6aa4d3ba63",
      "data": "0x608060806080608155"
    },
    "latest"
  ]
}
```

## eth_simulateV1

Executes a sequence of message calls building on each other's state without creating transactions on the block chain, optionally overriding block and state data

```json
{
    "jsonrpc": "2.0",
    "method": "eth_simulateV1",
    "params": [],
    "id": 0
}
```

## Fee market methods

- [eth/fee_market.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/fee_market.yaml)

## eth_gasPrice

Returns the current price per gas in wei.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_gasPrice",
  "params": []
}
```

## eth_blobBaseFee

Returns the base fee per blob gas in wei.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_blobBaseFee",
  "params": []
}
```

## eth_maxPriorityFeePerGas

Returns the current maxPriorityFeePerGas per gas in wei.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_maxPriorityFeePerGas",
  "params": []
}
```

## eth_feeHistory

Returns transaction base fee per gas and effective priority fee per gas for the requested/supported block range.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_feeHistory",
  "params": [
    "0x5",
    "latest",
    [
      20,
      30
    ]
  ]
}
```

## Filter methods

- [eth/filter.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/filter.yaml)

## eth_newFilter

Install a log filter in the server, allowing for later polling. Registers client interest in logs matching the filter, and returns an identifier.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_newFilter",
  "params": [
    {
      "fromBlock": "0x137d3c2",
      "toBlock": "0x137d3c3",
      "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "topics": []
    }
  ]
}
```

## eth_newBlockFilter

Creates a filter in the node, allowing for later polling. Registers client interest in new blocks, and returns an identifier.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_newBlockFilter",
  "params": []
}
```

## eth_newPendingTransactionFilter

Creates a filter in the node, allowing for later polling. Registers client interest in new transactions, and returns an identifier.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_newPendingTransactionFilter",
  "params": []
}
```

## eth_uninstallFilter

Uninstalls a filter with given id.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_uninstallFilter",
  "params": [
    "0x01"
  ]
}
```

## eth_getFilterChanges

Polling method for the filter with the given ID (created using `eth_newFilter`). Returns an array of logs, block hashes, or transaction hashes since last poll, depending on the installed filter.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getFilterChanges",
  "params": [
    "0x01"
  ]
}
```

## eth_getFilterLogs

Returns an array of all logs matching the filter with the given ID (created using `eth_newFilter`).

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getFilterLogs",
  "params": [
    "0x01"
  ]
}
```

## eth_getLogs

Returns an array of all logs matching the specified filter.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getLogs",
  "params": [
    {
      "fromBlock": "0x137d3c2",
      "toBlock": "0x137d3c3",
      "address": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "topics": []
    }
  ]
}
```

## Sign methods

- [eth/sign.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/sign.yaml)

## eth_sign

Returns an EIP-191 signature over the provided data.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_sign",
  "params": [
    "0x9b2055d370f73ec7d8a03e965129118dc8f5bf83",
    "0xdeadbeaf"
  ]
}
```

## eth_signTransaction

Returns an RLP encoded transaction signed by the specified account.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_signTransaction",
  "params": [
    {
      "data": "0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675",
      "from": "0xb60e8dd61c5d32be8058bb8eb970870f07233155",
      "gas": "0x76c0",
      "gasPrice": "0x9184e72a000",
      "to": "0xd46e8dd67c5d32be8058bb8eb970870f07244567",
      "value": "0x9184e72a"
    }
  ]
}
```

## State methods

## eth_getBalance

Returns the balance of the account of given address.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBalance",
  "params": [
    "0xfe3b557e8fb62b89f4916b721be55ceb828dbd73",
    "latest"
  ]
}
```

## eth_getStorageAt

Returns the value from a storage position at a given address.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getStorageAt",
  "params": [
    "0xfe3b557e8fb62b89f4916b721be55ceb828dbd73",
    "0x0",
    "latest"
  ]
}
```

## eth_getTransactionCount

Returns the nonce of an account in the state. NOTE: The name eth_getTransactionCount reflects the historical fact that an account's nonce and sent transaction count were the same. After the Pectra fork, with the inclusion of EIP-7702, this is no longer true.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionCount",
  "params": [
    "0xc94770007dda54cF92009BFF0dE90c06F603a09f",
    "latest"
  ]
}
```

## eth_getCode

Returns code at a given address.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getCode",
  "params": [
    "0xa50a51c09a5c451c52bb714527e1974b686d8e77",
    "latest"
  ]
}
```

## eth_getProof

Returns the merkle proof for a given account and optionally some storage keys.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getProof",
  "params": [
    "0xe5cB067E90D5Cd1F8052B83562Ae670bA4A211a8",
    [
      "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421"
    ],
    "latest"
  ]
}
```

## Submit methods

- [eth/submit.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/submit.yaml)

## eth_sendTransaction

Signs and submits a transaction.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_sendTransaction",
  "params": [
    {
      "from": "0xb60e8dd61c5d32be8058bb8eb970870f07233155",
      "to": "0xd46e8dd67c5d32be8058bb8eb970870f07244567",
      "gas": "0x76c0",
      "gasPrice": "0x9184e72a000",
      "value": "0x9184e72a",
      "input": "0xd46e8dd67c5d32be8d46e8dd67c5d32be8058bb8eb970870f072445675058bb8eb970870f072445675"
    }
  ]
}
```

## eth_sendRawTransaction

Submits a raw transaction. You can create and sign a transaction

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_sendRawTransaction",
  "params": [
    "0xf869018203e882520894f17f52151ebef6c7334fad080c5704d77216b732881bc16d674ec80000801ba02da1c48b670996dcb1f447ef9ef00b33033c48a4fe938f420bec3e56bfd24071a062e0aa78a81bf0290afbc3a9d8e9a068e6d74caa66c5e0fa8a46deaae96b0833"
  ]
}
```

## Transaction methods

- [eth/transaction.yaml](https://github.com/ethereum/execution-apis/blob/main/src/eth/transaction.yaml)

## eth_getTransactionByHash

Returns the information about a transaction requested by transaction hash.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByHash",
  "params": [
    "0xa52be92809541220ee0aaaede6047d9a6c5d0cd96a517c854d944ee70a0ebb44"
  ]
}
```

## eth_getTransactionByBlockHashAndIndex

Returns information about a transaction by block hash and transaction index position.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockHashAndIndex",
  "params": [
    "0xbf137c3a7a1ebdfac21252765e5d7f40d115c2757e4a4abee929be88c624fdb7",
    "0x2"
  ]
}
```

## eth_getTransactionByBlockNumberAndIndex

Returns information about a transaction by block number and transaction index position.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockNumberAndIndex",
  "params": [
    "0x1442e",
    "0x2"
  ]
}
```

## eth_getTransactionReceipt

Returns the receipt of a transaction by transaction hash.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionReceipt",
  "params": [
    "0x504ce587a65bdbdb6414a0c6c16d86a04dd79bfcc4f2950eec9634b30ce5370f"
  ]
}
```

## Debug methods

- [debug/getters.yaml]()

## debug_getRawHeader

Returns an RLP-encoded header.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_getRawHeader",
  "params": [
    "0x32026E"
  ]
}
```

## debug_getRawBlock

Returns an RLP-encoded block.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_getRawBlock",
  "params": [
    "0x32026E"
  ]
}
```

## debug_getRawTransaction

Returns an array of EIP-2718 binary-encoded transactions.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_getRawTransaction",
  "params": [
    "0x3a2fd1a5ea9ffee477f449be53a49398533d2c006a5815023920d1c397298df3"
  ]
}
```

## debug_getRawReceipts

Returns an array of EIP-2718 binary-encoded receipts.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_getRawReceipts",
  "params": [
    "0x32026E"
  ]
}
```

## debug_getBadBlocks

Returns an array of recent bad blocks that the client has seen on the network.

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_getBadBlocks",
  "params": []
}
```
