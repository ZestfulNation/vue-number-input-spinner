# vue-number-input-spinner
A customizable number input spinner component for Vuejs

## Demo
[https://zestfulnation.github.io/vue-number-input-spinner/](https://zestfulnation.github.io/vue-number-input-spinner/)

## Installation

* Install the package via NPM:

* `npm install vue-number-input-spinner`

* Load it in your project:

```javascript
import NumberInputSpinner from 'vue-number-input-spinner'

export default {
  components: {
    NumberInputSpinner,
  },
}
```

#### Usage example:
```html
<NumberInputSpinner
  :min="0"
  :max="10"
  :step="2"
  :inputClass="your-css-class"
  :buttonClass="your-other-css-class"
  :integerOnly="true"
  v-model="yourVModel"
  @change="onChange"
/>
```

## Events

The component emits the following events whenever its value changes, both receiving the new value and the previous value as arguments:

* `input` - used internally to support `v-model`.
* `change` - fired alongside `input` whenever the value changes, useful for consumers that prefer to listen with `@change` instead of relying on `v-model`.

```html
<NumberInputSpinner @change="onChange" @input="onInput" />
```
