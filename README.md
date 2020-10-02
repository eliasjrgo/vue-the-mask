# The Mask

A lightweight (2KB gzipped) and dependency free mask input created specific for Vue.js

FYI: 
This project is a copy of the original vue-the-mask project in https://github.com/vuejs-tips/vue-the-mask and its goal is to no longer have the error message "v-mask directive requires 1 input, found 0" as this message is displayed incorrectly in several cases that the component works smoothly.

## [Docs and Demo](https://vuejs-tips.github.io/vue-the-mask2)

## Install

```
npm i -S vue-the-mask2
```

## Usage (two flavors)

### Global

```javascript
import VueTheMask from 'vue-the-mask2'
Vue.use(VueTheMask2)
```

### Local (inside the component)

```javascript
import {TheMask} from 'vue-the-mask2'
export default {
  components: {TheMask}
}
```

### Local (as directive)

```javascript
import {mask} from 'vue-the-mask2'
export default {
  directives: {mask}
}
```

## Tokens

```javascript
'#': {pattern: /\d/},
'X': {pattern: /[0-9a-zA-Z]/},
'S': {pattern: /[a-zA-Z]/},
'A': {pattern: /[a-zA-Z]/, transform: v => v.toLocaleUpperCase()},
'a': {pattern: /[a-zA-Z]/, transform: v => v.toLocaleLowerCase()},
'!': {escape: true}
```

## Properties

| Property    | Required | Type                    | Default | Description                                |
|-------------|----------|-------------------------|---------|--------------------------------------------|
| value       | false    | String                  |         | Input value or v-model                     |
| mask        | **true** | String, Array           |         | Mask pattern                               |
| masked      | false    | Boolean                 | false   | emit value with mask chars, default is raw |
| placeholder | false    | String                  |         | Same as html input                         |
| type        | false    | String                  | 'text'  | Input type (email, tel, number, ...)       |
| tokens      | false    | Object                  | [tokens](#tokens) | Custom tokens for mask           |

## What about money?

We understand that money format is a totally different domain, which needs another specific component. You can use https://github.com/vuejs-tips/v-money

## License

This project is licensed under [MIT License](http://en.wikipedia.org/wiki/MIT_License)
