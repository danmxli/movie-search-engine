<script setup lang="ts"></script>

<template>
  <h1 class="hero-text">Movie Search Engine</h1>
  <p class="hero-tagline">Enter your input. Press <code>Search</code> to access the database</p>

  <div class="links">
    <div class="link-item">
      <a target="_blank" href="https://github.com/danmxli/movie-search-engine">Project Github</a>
    </div>
    <div class="link-item link-dot">•</div>
    <div class="link-item">
      <a target="_blank" href="https://github.com/danmxli">Central Repository Hub</a>
    </div>
  </div>

  <div class="features">
    <div class="feature-item">
      <article>
        <h2 class="title">Database</h2>
        <p class="detail">
          Implementing <span>MongoDB</span> as the NoSQL Database solution.
          Facilitates efficient and detailed resource fetching.
        </p>
      </article>
    </div>
    <div class="feature-item">
      <article>
        <h2 class="title">User Optimized Display</h2>
        <p class="detail">
          Returns <span>search results</span> in this format:  
        <ul>
          <li>Movie Poster</li>
          <li>Movie Title</li>
          <li>Movie Rating</li>
          <li>Movie Summary</li>
        </ul>
        </p>
      </article>
    </div>
    <div class="feature-item">
      <article>
        <h2 class="title">Continuous Improvement</h2>
        <p class="detail">
          The sky is the limit for this project! <br>
          Feel free to <a target="_blank" href="https://www.linkedin.com/in/danli591/">reach out to the Creator</a>. <br>  
          <span>Let's Connect and Innovate Together!</span>
        </p>
      </article>
    </div>
  </div>
</template>

<style lang="less">
@import './assets/css/styles.less';
</style>
