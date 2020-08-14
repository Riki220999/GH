# object-change-callsite

[![npm version][2]][3] [![build status][4]][5]
[![downloads][8]][9] [![js-standard-style][10]][11]

Determine the callsite of an object change using Proxies.

## Usage

```js
var onChange = require('object-change-callsite')

var state = {}
state = onChange(state, function (attr, value, callsite) {
  console.log(`${attr} changed to ${value} at ${callsite}`)
})

state.foo = 'hello'
state.bar = 'world'
```

## API

### `onChange(target, callback(attribute, value, callsite))`

Detect changes on the target object.
