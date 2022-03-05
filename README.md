# reactnative-firebase-sns-example
native firebase app.tsx

device subscription id is database register process

```javascript
  axios.get(apiUrl+'/api/auth-user',config).then(response => {
          messaging()
            .getToken(firebase.app().options.messagingSenderId)
            .then(x => registerDB(x,response.data.id))
            .catch(e => console.log(e));
           axios.get(apiUrl+'/api/usr/dashboard_stats',config).then(response => {
             panelProccess(response.data)
           });
        }).catch(error => {
           AsyncStorage.removeItem('user_local').then(response => {
              navigation.navigate("welcome")
           })
        });
```

```javascript
 .then(x => registerDB(x,response.data.id))
 ```
