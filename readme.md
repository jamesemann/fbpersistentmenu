# Facebook persistent menu

## 1 - Add a get started button

```curl -X POST -H "Content-Type: application/json" -d '{ 
  "get_started":{
    "payload":"this is the get started payload - it can be text, json, anything!"
  }
}' "https://graph.facebook.com/v2.6/me/messenger_profile?access_token=<PageAccessToken>"```

## 2 - Add your menu

```curl -X POST -H "Content-Type: application/json" -d '{
  "persistent_menu":[
    {
      "locale":"default",
      "composer_input_disabled":false,
      "call_to_actions":[
      {
          "type":"postback",
          "title":"Sample action",
          "payload": "this is the action payload - it can be text, json, anything!"
        }
      ]
    }  ]
}' "https://graph.facebook.com/v2.6/me/messenger_profile?access_token=<PageAccessToken"```