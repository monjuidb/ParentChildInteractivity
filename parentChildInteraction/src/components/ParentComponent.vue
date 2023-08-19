<script setup>
import {ref} from 'vue' 
import ChildComponent from './ChildComponent.vue';
const props=defineProps(['message'])
const parentMsg=ref('')
const childMsg='This is Parent component'

const UpdateParentMesage=()=>{
   
   parentMsg.value='Hello! This is child component'
}
</script>

<template>
   <div class="bg-green-400 w-[400px] h-[250px] mx-auto font-bold ">   
   <p class="my-5">
        <h2 class="text-xl">Parent Component</h2>
       Child message is {{ parentMsg }} 
    </p>
    <ChildComponent :childMessage="childMsg" @messageEmitted="UpdateParentMesage"/>
    </div>
</template>

<style scoped>

</style>
