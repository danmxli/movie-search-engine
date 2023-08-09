<script setup lang="ts">
import Safari from './components/Safari.vue'
</script>

<template>
  <h1 class="hero-text">Movie Search Engine</h1>
  <p class="hero-tagline">
    Enter your query. Press <code>&#x1F50E;&#xFE0E;</code> to fetch results!
  </p>

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
        <h2 class="title">Data Fetching</h2>
        <p class="detail">
          Provides accessibility to all up-to-date Movie data. <br />
          Efficient retreival with user-specified parameters enables a streamlined surfing
          experience.
        </p>
      </article>
    </div>
    <div class="feature-item">
      <article>
        <h2 class="title">User Optimized Display</h2>
        <p class="detail">
          Returns <span>search results</span> in this format:<br />
          > Movie Title <br />
          > Movie Description <br />
          > Movie Image
        </p>
      </article>
    </div>
    <div class="feature-item">
      <article>
        <h2 class="title">Improvements</h2>
        <p class="detail">
          <span>Lets connect and innovate together!</span> <br />
          > Continuous refinements for UI <br />
          > Development for GET,POST http methods <br />
          Feel free to
          <a target="_blank" href="https://www.linkedin.com/in/danli591/"
            >reach out to the Creator</a
          >.
        </p>
      </article>
    </div>
  </div>
  <Safari />
</template>

<style lang="less">
@import './assets/css/styles.less';
</style>
