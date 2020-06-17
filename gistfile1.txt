var axios = require('axios');
var qs = require('qs');
var data = qs.stringify({
 'payload': '{"channel": "#project-nodejs", "username": "webhookbot", "text": "Teste com Postman.", "icon_emoji": ":ghost:"}' 
});
var config = {
  method: 'post',
  url: 'https://hooks.slack.com/services/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',
  headers: { 
    'Content-Type': 'application/x-www-form-urlencoded'
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
