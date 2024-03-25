<template>
  <input type="text" v-model="userName" />
  <button @click="addUser">Ajouter</button>
  <ul>
    <li v-for="user in users">{{user}}</li>
  </ul>
</template>


<script setup>
import {ref} from "vue";

const users = ref(['Swann', 'Néo', 'Didou'])

const userName = ref("")
function addUser(){
  users.value.push(userName.value);
  userName.value = "";
}
</script>


<style scoped>
</style>
