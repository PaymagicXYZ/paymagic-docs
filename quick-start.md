# 🏎 Quick Start

## Example Payout

From a Smart Payout Account, customers can send out complex payouts with one simple API call:

* _/payout/disperse_ - Initiate a batch transfer of ERC-20 tokens
* _/payout/transfer_ - Initiate a simple transfer of tokens to a single recipient
* Coming Soon
  * _/payout/disperseNFT_ - Initiate a batch transfer of ERC-721 or ERc-1155 token
  * _/payout/airdrop_ - Initiate a MerkleDrop airdrop contract with claimable tokens
  * Cross-chain and cross-asset conversion

**Example POST /payout/disperse**

```jsx
var axios = require('axios');
var data = JSON.stringify({
  "assets": [
    "0xeb8f08a975Ab53E34D8a0330E0D34de942C95926"
  ],
  "amounts": [
    "100"
  ],
  "recipients": [
    "0x869eC00FA1DC112917c781942Cc01c68521c415e"
  ]
});

var config = {
  method: 'post',
  url: '<https://wwikf9fdp9.execute-api.us-east-1.amazonaws.com/test/v1/rin/account/0x7328285B4435dbc51897DC2d900D21707d14253e/payout/disperse>',
  headers: { 
    'Content-Type': 'application/json', 
    'X-API-KEY': '<Insert API Key>'
  },
  data : data
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});
```

