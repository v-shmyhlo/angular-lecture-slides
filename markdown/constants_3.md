Using constants

```js
// app/messenger/messenger.controller.js

// ...

MessengerController.$inject = ['ramda', 'messengerService'];
function MessengerController(R, messengerService) {
  var vm = this;

  // ...

  function getUnreadMessages() {
    // actually should be in filter, but good enough for illustration purposes
    return R.filter(R.prop('unread'), vm.messages);
  }
}
```
