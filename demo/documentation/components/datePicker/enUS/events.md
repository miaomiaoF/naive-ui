# Events
```html
<n-date-picker
  v-model="datetime"
  type="datetime"
  :disabled="disabled"
  @blur="onBlur1"
  @change="onChange1"
/>
<n-date-picker
  v-model="date"
  type="date"
  :disabled="disabled"
  @blur="onBlur2"
  @change="onChange2"
/>
<n-date-picker
  v-model="datetimerange"
  :disabled="disabled"
  type="datetimerange"
  @blur="onBlur3"
  @change="onChange3"
/>
<n-date-picker
  v-model="daterange"
  :disabled="disabled"
  type="daterange"
  @blur="onBlur4"
  @change="onChange4"
/>
<n-switch v-model="disabled" />
```
```js
export default {
  data() {
    return {
      datetime: 891360258000,
      date: null,
      datetimerange: [324910284, 910391323],
      daterange: [324910284, 910391323],
      disabled: false
    };
  },
  methods: {
    onBlur1 (v) {
      this.$NMessage.info('Blur1 ' + v)
    },
    onChange1 (v) {
      this.$NMessage.info('Change1 ' + v)
    },
    onBlur2 (v) {
      this.$NMessage.error('Blur2 ' + v)
    },
    onChange2 (v) {
      this.$NMessage.error('Change2 ' + v)
    },
    onBlur3 (v) {
      this.$NMessage.warning('Blur3 ' + v)
    },
    onChange3 (v) {
      this.$NMessage.warning('Change3 ' + v)
    },
    onBlur4 (v) {
      this.$NMessage.success('Blur4 ' + v)
    },
    onChange4 (v) {
      this.$NMessage.success('Change4 ' + v)
    }
  }
};
```
```css
.n-date-picker {
  margin: 0 12px 8px 0;
}
```