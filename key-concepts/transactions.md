# 💱 Transactions

Once you make a transaction, like a payout, the response is an [ethers.js](https://docs.ethers.io) [TransactionReponse](https://docs.ethers.io/v5/api/providers/types/#providers-TransactionResponse) with a `meta` field that has additional information. By default, the `meta` field comes back with a value of `{status: 'pending'}`.

The transaction status can then be queried via:

```
// {base}/v1 +
//    /{chain}/tx/{txhash}

const path = `https://api.paymagic.xyz/v1` +
    `/eth/tx/0xbec559f786cd24ff6acb188bd01fbd66472350679ad6f6ed163404809115a0d2` 
```

**meta Field**

The `meta` field provides further context about the transaction from Paymagic. For instance, if the transaction is a cross-chain swap, Paymagic will actually be making multiple blockchain transactions in the background. The `meta` field provides context back to the client with the status of the transaction:

**Status**

* `pending` - Transaction is being mined
* `in_transit` - Transaction requires multiple steps and is in-flight
* `paid` - Transaction is complete
* `failed` - Transaction failed and includes an error message
* `canceled` - Transaction has been canceled by the caller
