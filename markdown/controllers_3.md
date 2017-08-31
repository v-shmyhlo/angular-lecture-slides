Using controller

```html
<div id="app" ng-module="app">
  ...
  <div ng-controller="MessengerController as messenger">
    <div class="message-list">
      <div class="message" ng-repeat="message in messenger.messages">
        <span class="message-sender" ng-bind="message.sender"></span>
        <span class="message-body" ng-bind="message.body"></span>
      </div>
    </div>

    <div class="message-field">
      <messenger-message-field on-submit="messenger.sendMessage(message)"/>
    </div>
  </div>
  ...
</div>
```
