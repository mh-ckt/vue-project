<template>
  <a-collapse v-model:activeKey="activeKey" ghost v-for="item in list">
    <a-collapse-panel :key="item.key" :header="item.header">
      <component :is="item.components" />
    </a-collapse-panel>
  </a-collapse>
</template>

<script lang="ts" setup>
import { ref, watch } from 'vue'
import Card01 from '@/components/StyleSummary/card-01.vue'
let list = [
  {
    header: 'margin: auto的妙用',
    key: 1,
    components: Card01,
  },
]

const activeKey = ref(['1'])

watch(activeKey, (val) => {
  console.log(val)
})
</script>
