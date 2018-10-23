# awsapigateway
aws api gateway

## Install

```bash
npm install awsapigateway
```
## Quick Start


```js
const APIGatewayService = require('apigateway');
const apigw = new APIGatewayService({accessKeyId: 'myKey', secretAccessKey: 'mySercret'});

const uri = encodeURI('https://xxxx.execute-api.cn-northwest-1.amazonaws.com.cn/dev');
const options = {
  encoding: null,
  headers: {
    'Content-Type': 'application/json'
  },
  body: "{foo: 'bar'}"

}
apigw.post(uri, options, (err, res)=>{
  console.log(res.body);
})
```