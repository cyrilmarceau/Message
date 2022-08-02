<script setup>
import { ref, onMounted } from 'vue'

const props = defineProps({
  message: String
})


const message = ref('')


onMounted(() => {
    if(props.message !== undefined) {
        message.value = props.message
    }
})
</script>

<template>
  <p>{{message}}</p>
</template>

<style scoped>

</style>