Defining a controller

```js
// app/messenger/messenger.controller.js
angular
  .module('app.messenger')
  .controller('MessengerController', MessengerController);

MessengerController.$inject = ['messengerService'];
function MessengerController(messengerService) {
  var vm = this;
  vm.messages = [];
  vm.sendMessage = sendMessage;

  initialize();

  function initialize() {
    return messengerService.getMessages().then(function(res) {
      vm.messages = res.data;
    });
  }

  function sendMessage(message) {
    return messengerService.sendMessage(message);
  }
}
```
