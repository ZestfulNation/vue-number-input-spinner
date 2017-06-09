# vue-number-input-spinner
A customizable number input spinner component for Vuejs

## Installation

#### NPM

Install the package:

```
npm install vue-number-input-spinner
```

```javascript
import NumberInputSpinner from 'vue-number-input-spinner'

export default {
  components: {
    NumberInputSpinner,
  },
}
```

```html
<NumberInputSpinner
  :min="0"
  :max="10"
  @newNumber="someFunction"
/>
```
