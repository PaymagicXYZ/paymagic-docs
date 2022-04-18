---
description: List Accounts
---

# GET /accounts \[To Do]

Once you have a Smart Payout Account, you can initiate a batch transfer of ERC-20 tokens using the _/payout/disperse_ endpoint.

**Path**

```javascript
// Path Structure
//    /{chain}/account/{address} +
//    /payout/disperse

const dispersePath = `https://api.paymagic.xyz/v1` +
    `/eth/account/0xe9e284277648fcdb09b8efc1832c73c09b5ecf59` + 
    `/payout/disperse`
```

**Request Body**

Pass in three arrays corresponding to the payouts to make with this call:

* assets - array of token addresses to payout
* amounts - array of token amounts as strings, corresponding to assets array
* recipients - array of recipient addresses, corresponding to assets+amounts

```
var data = JSON.stringify({
  "assets": [
    "0xf52f827f0826959c173b34e8a2a63cb4c38c67c8",
    "0x375b18ec234e7801e79e49c76c468d86c331f22d"
  ],
  "amounts": [
    "100",
    "100"
  ],
  "recipients": [
    "0x869eC00FA1DC112917c781942Cc01c68521c415e",
    "0x0D79AfBF97a401968836b9D906F3f87b20d45A72"
  ]
});
```

Use the zero address for native tokens like ETH, MATIC, AVA

```
0x0000000000000000000000000000000000000000
```

**Response**

The response from payout endpoints is an [ethers.js](https://docs.ethers.io) [TransactionReponse](https://docs.ethers.io/v5/api/providers/types/#providers-TransactionResponse) with a `meta` field that has additional information. By default, the `meta` field comes back with a value of `{status: 'pending'}`.

For more information on the `meta` field, see the [Transactions page](../transactions.md).

```
{
  "meta": {
    "status": "pending"
  },
  "hash": "0x46c91fd81be30a3212daa3d9a2bdebd72ef63c343d59c381827cc3ccfaf91e24",
  "options": {
    "gasLimit": 8450000,
    "gasPrice": {},
    "from": "0x0D79AfBF97a401968836b9D906F3f87b20d45A72"
  },
  "transactionResponse": {
    "type": 2,
    "chainId": 4,
    "nonce": 203,
    "maxPriorityFeePerGas": {
      "type": "BigNumber",
      "hex": "0x4190aaf6"
    },
    "maxFeePerGas": {
      "type": "BigNumber",
      "hex": "0x4190aaf6"
    },
    "gasPrice": null,
    "gasLimit": {
      "type": "BigNumber",
      "hex": "0x80efd0"
    },
    "to": "0x7328285B4435dbc51897DC2d900D21707d14253e",
    "value": {
      "type": "BigNumber",
      "hex": "0x00"
    },
    "data": "0x6a761202000000000000000000000000a238cbeb142c10ef7ad8442c6d1f9e89e07e776100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000140000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000026000000000000000000000000000000000000000000000000000000000000000e48d80ff0a0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000009900eb8f08a975ab53e34d8a0330e0d34de942c9592600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000044a9059cbb000000000000000000000000869ec00fa1dc112917c781942cc01c68521c415e0000000000000000000000000000000000000000000000000000000005f5e100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000410000000000000000000000000d79afbf97a401968836b9d906f3f87b20d45a7200000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000",
    "accessList": [],
    "hash": "0x46c91fd81be30a3212daa3d9a2bdebd72ef63c343d59c381827cc3ccfaf91e24",
    "v": 1,
    "r": "0x5af403d2957eed0900abe62d3cb9b02256a3305618f2614d898094849ab15c77",
    "s": "0x2c6afaf7272952f85d00f3d44c9ac510a9fd47e1366c961c3867c4dcdfd61ffc",
    "from": "0x0D79AfBF97a401968836b9D906F3f87b20d45A72",
    "confirmations": 0
  }
}
```