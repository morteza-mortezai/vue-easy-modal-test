<script setup lang="ts">
import { openModal } from 'jenesius-vue-modal'
import VoidInvoice from '@/components/VoidInvoice.vue';
async function onOpen() {
  const props={name:'ali'}
  const modal = await openModal(VoidInvoice,props);
  modal.onclose = () => {
    alert('modal closed')
}
}
</script>

<template>
  <main>
    <button @click="onOpen">open modal</button>
  </main>
</template>
