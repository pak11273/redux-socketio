# Socket.io for Redux

## Table of contents
* [Install](#install)
* [Usage](#usage)
* [Options](#options)
* [Recipes](#recipes)
  * [Log only in development](#log-only-in-development)
* [To Do](#to-do)
* [Known issues](#known-issues)
* [License](#license)

## Install
`npm i -D redux-socketio`

`yarn i -D redux-socketio`

## Usage
```javascript
import { applyMiddleware, createStore } from 'redux';

// Middleware with default options
import ioMiddleware from 'redux-socketio'
const store = createStore(
  reducer,
  applyMiddleware(ioMiddleware)
)

// Note passing middleware as the third argument requires redux@>=3.1.0
```

## Options
```javascript
{
  meta: {
    ns:
    channel:
    room:
    }
}
```

### Options description

#### meta
Level of `console`. `warn`, `error`, `info` or [else](https://developer.mozilla.org/en/docs/Web/API/console).

meta property
* `ns`
* `channel`
* `room`

*Default: `log`*

#### __timestamp (Boolean)__

*Default: `true`*

## To Do
- [ ] Integrate webrtc for peer to peer connections 
- [ ] Implement airbnb linter [airbnb's](https://www.npmjs.com/package/eslint-config-airbnb)
- [ ] Write tests
- [ ] Node.js support
- [ ] React-native support

Feel free to create PR for any of those tasks!

## Known issues
* Performance issues in react-native ([#32](https://github.com/evgenyrodionov/redux-logger/issues/32))

## License
MIT
