<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref, onMounted } from 'vue'
import Message from './components/Message.vue'


const isSend = ref(false)

const sendMessage = () => {
  isSend.value = true
}

</script>

<template>

  <div>

    <Message />
    <Message message="Props de test" />


    <form action="">
        <textarea name="" id="" cols="30" rows="10">
          {{ isSend }}
        </textarea>
    </form>

     <button @click="sendMessage">Envoyer le message</button>
  </div>

  
</template>

<style scoped>
  div {
    display: flex;
    flex-direction: column;
  }
</style>
