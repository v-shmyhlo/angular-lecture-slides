Directive template

```html
<!-- app/core/app_counter.directive.html -->
<div class="counter">
  <div>Current value: {{ vm.counter }}</div>
  <button type="button" ng-click="vm.decrement()">Decrement</button>
  <button type="button" ng-click="vm.increment()">Increment</button>
</div>
```
