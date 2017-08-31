Using modules

```html
<body>
  <div id="app" ng-app="app">
    <div ng-controller="FeedController as feed">
      {{feed.unreadCount}}
    </div>

    <div ng-contoller="FriendsController as friends">
      <div ng-repeat="friend in friends.friends">
        ...
      </div>
    </div>
  </div>
</body>
```
