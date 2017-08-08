# vue-number-input-spinner
A customizable number input spinner component for Vuejs

## Demo
[https://krystalcampioni.github.io/vue-number-input-spinner/](https://krystalcampioni.github.io/vue-number-input-spinner/)

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
/>
```
