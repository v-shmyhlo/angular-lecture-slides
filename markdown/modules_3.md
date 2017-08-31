Complex example

```js
angular.module('app.core', []);
angular.module('app.utils', []);
angular.module('app.messenger', []);
angular.module('app.friends', []);
angular.module('app.feed', []);

var app = angular.module('app', [
  'app.core',
  'app.utils',
  'app.messenger',
  'app.friends',
  'app.feed',
]);
```
