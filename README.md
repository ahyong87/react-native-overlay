# react-native-overlay
---

## Usage

```js
'use strict';

var React = require('react-native');
var Overlay = require('./overlay');
var { AppRegistry, StyleSheet, View, Text } = React;

var  YApp  = React.createClass({
  getInitialState() {
      return {
        isOverlayOpen: true
      }
    },

  closeOverlay() {
    this.setState({isOverlayOpen: false});
  },

  render() {
    return (
      <View style={styles.page}>
 	<Overlay onPressBackdrop={this.closeOverlay} isVisible={this.state.isOverlayOpen} Opacity={0.5}/>
      </View>
    );
  }
});

var styles = StyleSheet.create({
  page: {
    flex: 1,
    position: 'absolute',
    bottom: 0,
    left: 0,
    right: 0,
    top: 0
  }
});

AppRegistry.registerComponent('App', () => App);
```


##API

### Overlay props

<table class="table table-bordered table-striped">
    <thead>
    <tr>
        <th style="width: 100px;">name</th>
        <th style="width: 50px;">type</th>
        <th style="width: 50px;">default</th>
        <th>description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
          <td>onPressBackdrop</td>
          <td>Function</td>
          <td>noop</td>
          <td>点击Overlay触发的回调函数</td>
        </tr>
        <tr>
            <td>isVisible</td>
            <td>Boolean</td>
            <th>true</th>
            <td>是否显示Overlay</td>
        </tr>
        <tr>
            <td>Opacity</td>
            <td>Int</td>
            <th>0.5</th>
            <td>Overlay透明度</td>
        </tr>
    </tbody>
</table>

**MIT Licensed**
