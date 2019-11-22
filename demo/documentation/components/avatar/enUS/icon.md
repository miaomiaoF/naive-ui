# Icon
```html
<n-avatar>
  <template v-slot:icon>
    <n-icon>
      <md-cash />
    </n-icon>
  </template>
</n-avatar>
```
```js
import mdCash from 'naive-ui/lib/icons/md-cash'
import mdContacts from 'naive-ui/lib/icons/md-contacts'
import iosContacts from 'naive-ui/lib/icons/ios-contacts'

export default {
  components: {
    mdCash,
    mdContacts,
    iosContacts
  }
}
```