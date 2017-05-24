SpringEdge REST API for Node.js
================================

This repository contains A nodejs RestAPI package to send sms using Spring Edge APIs

Requirements
------------

- [Sign up](https://www.springedge.com/) for a free Trail Messaging account
- Create a new `apikey` from developers section of sms account
- Setup sender name for sms account.
- SpringEdge REST API for Node.js requires Node.js >= 0.10 or io.js


Installation
------------

`npm install springedge`


Usage
-----
Example of sending message:

```javascript
var springedge = require('springedge');
```

```javascript
// send sms

var springedge = require('springedge');

var params = {
  'apikey': '', // API Key
  'sender': 'SEDEMO', // Sender Name
  'to': [
    '919019xxxxxxxx'  //Moblie Number
  ],
  'body': 'test+message'
};

springedge.messages.send(params, function (err, response) {
  if (err) {
    return console.log(err);
  }
  console.log(response);
});

// Result:
{
  "groupID":xxxx,
  "MessageIDs":"xxxxx-x",
  "status":"AWAITED-DLR"
}
```

Or in case of an error:

```javascript
{
  "error":"Invalid Mobile Numbers"
}
```


Support
-------------

For any support or instructions please visit below website:
[https://www.springedge.com](https://www.springedge.com)