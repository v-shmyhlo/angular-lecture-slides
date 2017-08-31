More examples

```js
// app/core/app_counter.directive.js
angular
  .module('app.core')
  .directive('appCounter', appCounter);

function appCounter() {
  var directive = {
    restrict: 'EA',
    templateUrl: 'app/core/app_counter.directive.html',
    scope: {},
    controller: CounterController,
    controllerAs: 'vm',
    bindToController: true
  };

  return directive;
}

function CounterController($scope) {
  var vm = this;
  vm.counter = 0;
  vm.increment = increment;
  vm.decrement = decrement;

  function inrement() {
    vm.counter += 1;
  }

  function decrement() {
    vm.increment -= 1;
  }
}
```
