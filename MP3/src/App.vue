<script>

import ContentFeed from './ContentFeed.vue'
import LeftNavbar from './LeftNavbar.vue'
import RightNavbar from './RightNavbar.vue'
import StoryCarousel from './StoryCarousel.vue'
import TopNavbar from './TopNavbar.vue'

export default {
  name: 'App',
  components: {
    ContentFeed,
    LeftNavbar,
    RightNavbar,
    StoryCarousel,
    TopNavbar
  }
}
</script>


<template>
  <div id="app">
    <header>
      <h1>Facebook</h1>
    </header>
    <main>
      <section class="news-feed">
        <h2>News Feed</h2>
        <!-- Add more content to mimic the Facebook homepage -->
        <ContentFeed />
        <LeftNavbar />
        <RightNavbar />
        <StoryCarousel />
        <TopNavbar />
      </section>
    </main>
  </div>
</template>



<style>
#app {
  font-family: "Arial", sans-serif;
  text-align: center;
  color: #1c1e21;
  margin-top: 60px;
}

header {
  background-color: #4267b2;
  color: #fff;
  padding: 10px;
}

main {
  max-width: 600px;
  margin: 0 auto;
}

.news-feed {
  /* Add styles for the News Feed section */
}
</style>
