## 安装

```
npm install v-hotkey-yyf --save
```
## 使用

### 1、引入

```
import VueHotkey from 'v-hotkey-yyf'
```
```
Vue.use(VueHotkey)
```

### 2、配置

```
<template lang='pug'>
   <input v-hotkey="{keymap:keymap,isfull: false}" v-show="showing" />
</template>

<script>
export default {
  data () {
    return {
      showing: true
    }
  },
  methods: {
    keymaphandler () {
      alert('111')
    }
  },
  computed: {
    keymap () {
      return {
        'ctrl+enter': this.keymaphandler
      }
    }
  }
}
</script>
```
### 3、参数详解

**keymap：**

类型 Object
eg：'ctrl+enter': this.keymaphandler [键位]:[回调]


**isfull：**

类型 Boolean
eg: isfull:false [全局可用即document/绑定到当前的元素]