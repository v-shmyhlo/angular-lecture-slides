Defining a directive

```js
// app/messenger/messenger_message_field.directive.js
angular
  .module('app.messenger')
  .directive('messengerMessageField', messengerMessageField);

function messengerMessageField() {
  var directive = {
    link: link,
    templateUrl: '/app/messenger/messenger_message_field.directive.html',
    restrict: 'EA'
  };

  return directive;

  function link(scope, element, attrs) {
    // ...
  }
}
```
