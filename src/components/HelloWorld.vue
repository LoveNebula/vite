<script setup>
import { ref } from 'vue'

defineProps({
  msg: {
    type:String,
    default:''
  },
  init:{
    type:Number,
    default:22
  }
})
let emit  = defineEmits(["goERS"])
const count = ref(0)

const goER = () => {
  emit("goERS", '你好')
}
</script>

<template>

  <h1>{{ msg }}</h1>
  <h1>{{ init }}</h1>

  <div class="card">
<!--    <button type="button" @click="count++">count is {{ count }}</button>-->
    <el-button @click="count++">新增</el-button>
    count的值为{{count}}

    <el-button @click="goER">gigigi</el-button>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
