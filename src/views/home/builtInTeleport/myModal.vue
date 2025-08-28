<script setup>
import { ref } from 'vue'
const open = ref(false)
</script>

<template>
  <button @click="open = true"><span>Open Modal</span></button>
  <!-- <Teleport to="body"> -->
  <div v-if="open" class="modal">
    <div class="content">
      <p>Hello from the modal!</p>
      <button @click="open = false"><span>Close</span></button>
    </div>
  </div>
  <!-- </Teleport> -->
</template>

<style scoped lang="less">
button {
  font-size: 14px;
  height: 32px;
  padding: 4px 15px;
  border-radius: 6px;
  border: 1px solid transparent;
  color: #fff;
  background-color: #8FBC8F;
  box-shadow: 0 2px 0 rgba(5, 145, 255, 0.1);
  cursor: pointer;

  span {
    display: inline-block;
    white-space: nowrap;
    text-align: center;
  }
}

.modal {
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.45);

  .content {
    width: 300px;
    position: absolute;
    background-color: #fff;
    border-radius: 10px;
    padding: 10px;
    top: 30%;
    left: 50%;
    transform: translateX(-50%);
  }
}
</style>