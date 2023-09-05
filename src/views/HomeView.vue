<script setup lang="ts">
import {defineAsyncComponent} from 'vue'
import { openModal } from 'jenesius-vue-modal'
// import VoidInvoice from '@/components/VoidInvoice.vue';
const VoidInvoice = defineAsyncComponent(() =>
  import( '@/components/VoidInvoice.vue')
)
async function onOpen() {
  const props = { name: 'ali' }
  const modal = await openModal(VoidInvoice, props);
  modal.onclose = () => {
    //refresh page
  }
}
</script>

<template>
  <main>
    <button @click="onOpen">open modal</button>
  </main>
</template>
