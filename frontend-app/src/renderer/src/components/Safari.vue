<script>
import '../assets/css/search.css';
import { ref } from 'vue';

export default {
  name: 'Safari',
  setup() {
    const counter = ref(0);
    return {
      counter
    };
  }
}
</script>

<template>
  <div class="container">
    <div class="search-bar">
      <input type="text" class="search-input" placeholder="Enter your query">
      <button class="search-button" @click="counter++">&#x1F50E;&#xFE0E;</button>
    </div>
  </div>
  <div class="query-count">
    <p>
      <b>Number of Queries: {{ counter }}</b>
    </p>
  </div>
</template>
