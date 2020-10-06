# 对话框 Dialog
执行之前，请确认。

## 演示
```demo
basic
async
use-component
```

## API
### Dialog Injection API
|名称|类型|说明|
|-|-|-|
|warning|`(options: DialogOption) => DialogReactive`||
|success|`(options: DialogOption) => DialogReactive`||
|error|`(options: DialogOption) => DialogReactive`||
|destroyAll|`() => void`||

### DialogOption API
|名称|类型|默认值|说明|
|-|-|-|-|
|theme|`'light' \| 'dark' \| null \| string`|`null`||
|type|`'error \| 'success' \| 'warning'`|`'warning'`||
|title|`string \| (() => VNode \| Array<VNode>)`|`null`|可以是 render 函数|
|closable|`boolean`|`true`||
|icon|`() => VNode \| Array<VNode>`|`null`|需要是 render 函数|
|negative-text|`string`|`null`|不填对应的按钮不会出现|
|positive-text|`string`|`null`|不填对应的按钮不会出现|
|content|`string \| (() => VNode \| Array<VNode>)`|`null`|可以是 render 函数|
|show-icon|`boolean`|`true`||
|loading|`boolean`|`false`||
|bordered|`boolean`|`false`||
|onPositiveClick|`() => boolean \| Promise<boolean> \| any`|`() => true`|默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为|
|onNegativeClick|`() => boolean \| Promise<boolean> \| any`|`() => true`|默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为|
|onClose|`() => boolean \| Promise<boolean> \| any`|`() => true`|默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为|

### DialogReactive API
#### DialogReactive Properties
下列属性都可以被动态修改。

|名称|类型|说明|
|-|-|-|
|theme|`'light' \| 'dark'`||
|type|`'error \| 'success' \| 'warning'`||
|title|`string \| (() => VNode \| Array<VNode>)`|可以是 render 函数|
|closable|`boolean`||
|icon|`() => VNode \| Array<VNode>`|需要是 render 函数|
|negative-text|`string`|不填对应的按钮不会出现|
|positive-text|`string`|不填对应的按钮不会出现|
|content|`string \| (() => VNode \| Array<VNode>)`|可以是 render 函数|
|show-icon|`boolean`||
|loading|`boolean`||
|bordered|`boolean`||
|onPositiveClick|`() => boolean \| Promise<boolean> \| any`||
|onNegativeClick|`() => boolean \| Promise<boolean> \| any`||
|onClose|`() => boolean \| Promise<boolean> \| any`||

#### DialogReactive Methods
|名称|类型|说明|
|-|-|-|
|destroy|`()`|关闭 Dialog|

## Props
### Dialog Props
|名称|类型|默认值|说明|
|-|-|-|-|
|type|`'error \| 'success' \| 'warning'`|`'warning'`||
|title|`string \| (() => VNode \| Array<VNode>)`|`null`|可以是 render 函数|
|closable|`boolean`|`boolean`||
|icon|`() => VNode \| Array<VNode>`|`null`|需要是 render 函数|
|negative-text|`string`|`null`|不填对应的按钮不会出现|
|positive-text|`string`|`null`|不填对应的按钮不会出现|
|content|`string \| (() => VNode \| Array<VNode>)`|`null`|可以是 render 函数|
|show-icon|`boolean`|`true`||
|loading|`boolean`|`false`||
|bordered|`boolean`|`false`||
|on-positive-click|`() => any`||
|on-negative-click|`() => any`||
|on-close|`() => any`||

## Events
### Confirm Events
|名称|参数|说明|
|-|-|-|
|positive-click|`()`||
|negative-click|`()`||
|close|`()`||

## Slots
### Confirm Slots
|名称|参数|说明|
|-|-|-|
|icon|`()`||
|header|`()`||
|default|`()`|内容|
|action|`()`||
