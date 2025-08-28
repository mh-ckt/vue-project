<script setup lang="ts">
import MyModal from './myModal.vue';
import AntdvModal from './antdvModal.vue';
</script>

<template>
  <div class="modal-wrap">
    <p>Teleport</p>
    <MyModal />
    <AntdvModal />
  </div>

</template>

<style lang="less" scoped>
.modal-wrap {
  // position: absolute;
  // left: 50%;
  // top: 0;
  // transform: translateX(-50%);
  // display: flex;
  // align-items: center;
  // gap: 10px;

  p {
    white-space: nowrap;
    font-size: 2rem;
  }
}
</style>
