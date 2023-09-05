<template>
    <div class="modal">
        <h1>
    
            Hello {{ name }}
            I am Modal
        </h1>
        <button @click="onClose">close</button>
    </div>
</template>
<script setup lang="ts">
import {onMounted} from 'vue'
import { closeModal } from 'jenesius-vue-modal'
const props=defineProps(['name'])
function onClose(){
    closeModal()
}
onMounted(()=>{
    console.log('props',props.name)
})
</script>
<style>
.modal{
    background-color: white;
    border: 1px solid black;
    padding: 30px;
}
</style>