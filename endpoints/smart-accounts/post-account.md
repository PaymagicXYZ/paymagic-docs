---
description: Create Account
---

# POST /account

Once you have an API Key, you can create a "Smart Account", aka deploys a new Gnosis Safe that you can control through Paymagic.

Technically, the endpoint creates a [Proxy Contract through the Gnosis Safe SDK](https://docs.gnosis-safe.io/build/sdks/core-sdk) and adds the signer parameter and Paymagic as signers with a 1 of 2 threshold. No [Zodiac modules](https://gnosis.github.io/zodiac/docs/intro#what-is-zodiac) are deployed for the Safe by default.

**Path**

```javascript
// Path Structure
//    /{chain}/account

const createAccountPath = `https://api.paymagic.xyz/v1` +
    `/eth/account`
```

**Request Body**

Pass in a signer that has rights to the Safe.&#x20;

{% hint style="danger" %}
The signer address MUST be secure and CANNOT have a compromised private key, otherwise, your funds are at risk. We recommend using a hardware wallet, like a [Ledger](https://www.ledger.com) or a [Trezor](https://trezor.io), for the signer address.
{% endhint %}

* signer - signer addresses that you or your customers securely control

```
var data = JSON.stringify({
  "signer": "0x869eC00FA1DC112917c781942Cc01c68521c415e"
});
```

**Response**

The response from the create account endpoint returns the new Gnosis Safe address and transaction hash.

```
{
  transactionHash: 0x08a39a3e2fb37caf1eb196c68890f5e9ca3841be5215fd5f2fed6be2f105f473,
  safeAddress: 0x375b18ec234d7801e79e49c76c468d86c331f22d
}
```
