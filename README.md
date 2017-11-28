# Socket.io for Redux

## Table of contents
* [Install](#install)
* [Usage](#usage)
* [Options](#options)
* [Recipes](#recipes)
  * [Log only in development](#log-only-in-development)
* [To Do](#to-do)
* [Known issues](#known-issues) (with `react-native` only at this moment)
* [License](#license)

## Install
`npm i -D redux-socketio`
`yarn i -D redux-socketio`

## Usage
```javascript
import { applyMiddleware, createStore } from 'redux';

// Logger with default options
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

#### __level (String | Function | Object)__
Level of `console`. `warn`, `error`, `info` or [else](https://developer.mozilla.org/en/docs/Web/API/console).

It can be a function `(action: Object) => level: String`.

It can be an object with getter functions: `prevState`, `action`, `nextState`, `error`. Useful if you want to print
message based on specific state or action. Set any of them to `false` if you want to hide it.

* `prevState(prevState: Object) => level: String`
* `action(action: Object) => level: String`

*Default: `log`*

#### __timestamp (Boolean)__
Print timestamp with each action?

*Default: `true`*

#### __colors (Object)__
Object with color getter functions: `title`, `prevState`, `action`, `nextState`, `error`. Useful if you want to paint
message based on specific state or action. Set any of them to `false` if you want to show plain message without colors.

* `title(action: Object) => color: String`
* `prevState(prevState: Object) => color: String`

## To Do
- [x] Update eslint config to [airbnb's](https://www.npmjs.com/package/eslint-config-airbnb)
- [ ] Clean up code, because it's very messy, to be honest
- [ ] Write tests
- [ ] Node.js support
- [ ] React-native support

Feel free to create PR for any of those tasks!

## Known issues
* Performance issues in react-native ([#32](https://github.com/evgenyrodionov/redux-logger/issues/32))

## License
MIT
