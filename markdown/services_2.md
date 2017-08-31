Defining a service

```js
// app/messenger/messenger.service.js
angular
  .module('app.messenger')
  .service('messengerService', messengerService);

messengerService.$inject = ['$http'];
function messengerService($http) {
  this.getMessages = getMessages;

  function getMessages() {
    return $http.get('api/v1/messages');
  }
}
```
