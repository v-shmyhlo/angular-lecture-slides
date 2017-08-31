Main purpose of modules is to register (bundle) components to provide them for future use by other
modules, components

```js
// app/feed/feed.controller.js
angular
  .module('app.feed')
  .controller('FeedController', FeedController);

function FeedController() {
  // ...
}
```

```js
// app/utils/logger.factory.js
angular
  .module('app.utils')
  .factory('logger', logger);

function logger() {
  // ...
}
```
