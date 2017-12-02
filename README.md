# Socket.io for Redux

This module is built on top of zurfyx's implementation found ([here](https://stackoverflow.com/questions/37876889/react-redux-and-websockets-with-socket-io))

## Table of contents
* [Install](#install)
* [Usage](#usage)
* [To Do](#to-do)
* [Known issues](#known-issues)
* [License](#license)

## Install
`npm i -D redux-socketio` or `yarn i -D redux-socketio`

## Usage
```javascript
import Socket from './services/socketio/index.js'
import {createStore, applyMiddleware} from 'redux'
import ioMiddleware from 'redux-socketio'
const SocketClient = new Socket()

const store = createStore(
  ... 
      applyMiddleware(ioMiddleware(SocketClient))
  ... 
)

...

export default store

// Note passing middleware as the third argument requires redux@>=3.1.0
```

## See [wiki](https://github.com/pak11273/redux-socketio/wiki) for more details 

## To Do
- [ ] Write tests
- [ ] Node.js support
- [ ] React-native support

Feel free to create PR for any of those tasks!

## Known issues
* Performance issues ([#1](https://github.com/pak11273/redux-socketio/issues/1))

## License
MIT
