# 🏎 Quick Start

## Example Payout

From a Smart Payout Account, customers can send out complex payouts with one simple API call:

* _/payout/disperse_ - Initiate a batch transfer of ERC-20 tokens to multiple recipients
* _/payout/transfer_ - Initiate a simple transfer of ERC-20 tokens to a single recipient

The path for the request is structured as:

```javascript
POST https://api.paymagic.xyz/v1/{chain}/account/{address}/payout/disperse
```

Body data:

```
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
```

**Example POST /payout/disperse**

```jsx
var axios = require('axios');
var data = JSON.stringify({
  "assets": [
    "0xeb8f08a975Ab53E34D8a0330E0D34de942C95926",
    "0xeb8f08a975Ab53E34D8a0330E0D34de942C95926"
  ],
  "amounts": [
    "10",
    "10"
  ],
  "recipients": [
    "0x869eC00FA1DC112917c781942Cc01c68521c415e",
    "0x0D79AfBF97a401968836b9D906F3f87b20d45A72"
  ]
});

var config = {
  method: 'post',
  url: 'https://api.paymagic.xyz/v1/rin/account/0x7328285B4435dbc51897DC2d900D21707d14253e/payout/disperse>',
  headers: { 
    'Content-Type': 'application/json', 
    'X-API-KEY': 'LiSIgRO38P54sBskeaAtkZnrDGTAKEc1amq4W654' // Test API Key
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

