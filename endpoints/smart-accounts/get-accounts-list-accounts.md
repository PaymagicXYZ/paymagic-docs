---
description: List Accounts
---

# GET /accounts - List Accounts

You can list all the Smart Accounts that your API Key controls with this endpoint.

**Path**

```javascript
// Path Structure
//    /accounts

const listAccountsPath = `https://api.paymagic.xyz/v1` +
    `/accounts`
```

**Response**

The response will be an array of all accounts your API Key controls on all chains..

```
{[
  eth:0x550abC18F49CB82644dF58885A3A049A021D54e0,
  matic:0x375b18ec234d7801e79e49c76c468d86c331f22d
]}
```
