
## react-native-scrollable-tab-view
[![npm version](https://badge.fury.io/js/react-native-scrollable-tab-view.svg)](https://badge.fury.io/js/react-native-scrollable-tab-view)

This is probably my favorite navigation pattern on Android, I wish it
were more common on iOS! This is a very simple JavaScript-only
implementation of it for React Native. For more information about how
the animations behind this work, check out the Rebound section of the
[React Native Animation Guide](https://facebook.github.io/react-native/docs/animations.html)


## Add it to your project

1. Run `npm install react-native-scrollable-tab-view --save`
2. `var ScrollableTabView = require('react-native-scrollable-tab-view');`

## Basic usage

```javascript
var ScrollableTabView = require('react-native-scrollable-tab-view');

var App = React.createClass({
  render() {
    return (
      <ScrollableTabView>
        <ReactPage tabLabel="React" />
        <FlowPage tabLabel="Flow" />
        <JestPage tabLabel="Jest" />
      </ScrollableTabView>
    );
  }
});
```

## Injecting a custom tab bar

Suppose we had a custom tab bar called `CustomTabBar`, we would inject
it into our `ScrollableTabView` like this:

```javascript
var ScrollableTabView = require('react-native-scrollable-tab-view');
var CustomTabBar = require('./CustomTabBar');

var App = React.createClass({
  render() {
    return (
      <ScrollableTabView renderTabBar={() => <CustomTabBar someProp={'here'} />}>
        <ReactPage tabLabel="React" />
        <FlowPage tabLabel="Flow" />
        <JestPage tabLabel="Jest" />
      </ScrollableTabView>
    );
  }
});
```
To start you can just copy [DefaultTabBar](https://github.com/eden120/reactnative-scrollable-tabview/blob/master/DefaultTabBar.js).

## Examples

[SimpleExample](https://github.com/eden120/reactnative-scrollable-tabview/blob/master/Example/SimpleExample.js).

[ScrollableTabsExample](https://github.com/eden120/reactnative-scrollable-tabview/blob/master/Example/ScrollableTabsExample.js).

[OverlayExample](https://github.com/eden120/reactnative-scrollable-tabview/blob/master/Example/OverlayExample.js).

[FacebookExample](https://github.com/eden120/reactnative-scrollable-tabview/blob/master/Example/FacebookExample.js).


## Contribution
**Issues** are welcome. Please add a screenshot of bug and code snippet. Quickest way to solve issue is to reproduce it on one of the examples.

**Pull requests** are welcome. If you want to change API or making something big better to create issue and discuss it first. Before submiting PR please run ```eslint .``` Also all eslint fixes are welcome.

Please attach video or gif to PR's and issues it is super helpful.

---

