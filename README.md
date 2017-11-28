# Socket.io for Redux

# This is my first npm library.  The current version is not ready for any type of production use.  Use for experimental purposes only!

## Table of contents
* [Install](#install)
* [Usage](#usage)
* [Options](#options)
* [Examples](#examples)
  * [with webrtc](#with-webrtc)
* [To Do](#to-do)
* [Known issues](#known-issues)
* [License](#license)

## Install
`npm i -D redux-socketio` or `yarn i -D redux-socketio`

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

## Examples

## with webrtc

## To Do
- [ ] Users can see a list of channels provided by remote server 
- [ ] Users can join a channel 
- [ ] Users can generate rooms 
- [ ] Users can private message other users 
- [ ] Users will be notified of friends status(online, offline, afk, etc) 
- [ ] Integrate webrtc for peer to peer connections 
- [ ] Implement airbnb linter [airbnb's](https://www.npmjs.com/package/eslint-config-airbnb)
- [ ] Write tests
- [ ] Node.js support
- [ ] React-native support

Feel free to create PR for any of those tasks!

## Known issues
* Performance issues in react-native ([#32](https://github.com/pak11273/redux-socketio/issues/1))

## License
MIT
