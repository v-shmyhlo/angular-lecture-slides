Dependency injection

```js
// app/messenger/messenger.module.js
angular.module('app.messenger', []);

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

// app/messenger/messenger.controller.js
angular
  .module('app.messenger')
  .controller('MessengerController', MessengerController);

MessengerController.$inject = ['messengerService', 'logger', '$timeout'];
function MessengerController(messengerService, logger, $timeout) {
  initialize();

  function initialize() {
    $timeout(function() {
      messengerService.getMessages().then(function(res) {
        logger.debug(res.data);
      });
    }, 500);
  }
}
```
