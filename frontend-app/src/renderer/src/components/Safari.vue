<script>
import '../assets/css/search.css'
import { ref } from 'vue'

export default {
  name: 'Safari',
  setup() {
    const counter = ref(0)
    const userInput = ref('')
    const output = ref({})

    function fetchData() {
      if (userInput.value != '') {
        counter.value++
        console.log(userInput.value)

        const options = {
          method: 'GET',
          headers: {
            accept: 'application/json',
            Authorization:
              'Input Your Authorization'
          }
        }

        fetch(
          `https://api.themoviedb.org/3/search/movie?query=${userInput.value}&include_adult=false&language=en-US&page=1`,
          options
        )
          .then((response) => response.json())
          .then((data) => {
            if (data) {
              output.value = Object.values(data)[1]

              // logging purposes
              console.log(Object.values(data)[1])

              // iterate through array of objects
              for (let i = 0; i < Object.values(data)[1].length; i++) {
                // assign poster string value
                if (Object.values(data)[1][i].poster_path !== null) {
                  Object.values(data)[1][i].poster_path =
                    'https://image.tmdb.org/t/p/original' + Object.values(data)[1][i].poster_path
                } 
                else {
                  Object.values(data)[1][i].poster_path =
                    'https://via.placeholder.com/600x900/24292e/6cc644?text=No+Poster'
                }

                if (Object.values(data)[1][i].overview == '') {
                  Object.values(data)[1][i].overview = 'No overview provided.'
                }
                const words = Object.values(data)[1][i].overview.split('')
                if (words.length > 250) {
                  Object.values(data)[1][i].overview = words.slice(0, 250).join('') + '...'
                }
              }
            }
          })
          .catch((err) => console.error(err))
      }
    }
    return {
      counter,
      userInput,
      fetchData,
      output
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="search-bar">
      <input v-model="userInput" type="text" class="search-input" placeholder="Enter your query" />
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
  <div class="features">
    <div v-for="movie in output" :key="movie.id" class="feature-item">
      <article>
        <div class="description-container">
          <h3>{{ movie.title }}</h3>
          <br />
          <p class="detail">{{ movie.overview }}</p>
          <br />
        </div>
        <div class="img-container">
          <img :src="movie.poster_path" />
        </div>
      </article>
    </div>
  </div>
</template>
