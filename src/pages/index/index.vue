<template>
  <view class="container">
    <nut-popover v-model:visible="visible.darkTheme" theme="dark" location="bottom-start" :list="iconItemList">
      <template #reference>
        <view class="switch">
          <text>切换</text>
        </view>
      </template>
    </nut-popover>


  </view>



</template>
<script setup>
import { reactive, ref } from "vue"
const visible = ref({
  darkTheme: false,
  lightTheme: false,
})
const iconItemList = reactive([
  { name: '选项一' },
  { name: '选项二' },
  { name: '选项三' }
])
</script>
<style>
.container {
  background-color: teal;
  height: 500px;
  position: relative;
}

.container .switch {
  position: absolute;
  top: 400px;
  left: 600px;
}
</style>
