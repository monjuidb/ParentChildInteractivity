<script setup>
const props=defineProps(['childMessage'])
defineEmits(['messageEmitted'])
</script>

<template>
  <p class="my-5">
        <h2 class="text-xl">Child Component</h2>
        Parent Message : {{ props.childMessage }} 
  </p>
    <p class="mx-auto" >
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded my-5 w-48"
        @click="$emit('messageEmitted')">Show Message</button>  
       
    </p>
</template>

<style scoped>

</style>
