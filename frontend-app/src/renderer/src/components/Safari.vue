<script>
import '../assets/css/search.css';
import { ref } from 'vue';

export default {
  name: 'Safari',
  setup() {
    const counter = ref(0);
    const userInput = ref('');

    function fetchData() {
      if (userInput.value != "") {
        counter.value++
        console.log(userInput.value);
      }
    };

    return {
      counter,
      userInput,
      fetchData
    };
  }
}
</script>

<template>
  <div class="container">
    <div class="search-bar">
      <input v-model="userInput" type="text" class="search-input" placeholder="Enter your query">
      <button class="search-button" @click="fetchData">&#x1F50E;&#xFE0E;</button>
    </div>
  </div>
  <div class="query-indicator">
    <p>
      <b>
        Number of Queries: {{ counter }} <br />
        User Input: "{{ userInput }}"
      </b>
    </p>
  </div>
</template>
