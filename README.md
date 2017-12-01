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
import { applyMiddleware, createStore } from 'redux';
import socketClient from './socketClient';

// Middleware with default options
import ioMiddleware from 'redux-socketio'
const store = createStore(
  ...
  applyMiddleware(ioMiddleware(socketClient))
  ...
)

// Note passing middleware as the third argument requires redux@>=3.1.0
```

## See wiki for more details 

## To Do
- [ ] Write tests
- [ ] Node.js support
- [ ] React-native support

Feel free to create PR for any of those tasks!

## Known issues
* Performance issues ([#1](https://github.com/pak11273/redux-socketio/issues/1))

## License
MIT
