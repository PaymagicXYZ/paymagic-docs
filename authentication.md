# ▶ Authentication

The Paymagic Automate API requires an API Key to access any of the endpoints. In the future, we may add additional methods of authentication and authorization like [OAuth](https://oauth.net/) or [signed messages from Ethereum Addresses](https://login.xyz/).

The Paymagic Team will provide customers with an API Key, which must be kept safe and secure. Access to a customer's API Key can result in the loss of funds.

Pass the API Key into the `X-API-KEY` Header for each request:

```javascript
var axios = require('axios');
var data = JSON.stringify({});

var config = {
  headers: { 
    'Content-Type': 'application/json', 
    'X-API-KEY': '<Insert API Key>'
  },
  method: 'post',
  url: 'https://api.paymagic.xyz/v1/rin/account/0x7328285B4435dbc51897DC2d900D21707d14253e/payout/disperse',
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
