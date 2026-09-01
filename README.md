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
  :debounce="500"
  v-model="yourVModel"
/>
```

#### Props

| Prop | Type | Default | Description |
| --- | --- | --- | --- |
| `min` | Number | `0` | Minimum allowed value |
| `max` | Number | `10` | Maximum allowed value |
| `step` | Number | `1` | Amount to increase/decrease on each click |
| `mouseDownSpeed` | Number | `100` | Interval (ms) between increments while the button is held down |
| `debounce` | Number | `0` | Delay (ms) before the `input` event is emitted, useful to avoid emitting on every increment while holding down a button. Defaults to `0` (no debounce, event fires immediately) |
| `inputClass` | String | `vnis__input` | CSS class applied to the input element |
| `buttonClass` | String | `vnis__button` | CSS class applied to the buttons |
| `integerOnly` | Boolean | `false` | Restrict typed input to integers only |
| `disabled` | Boolean | `false` | Disable the input and buttons |
