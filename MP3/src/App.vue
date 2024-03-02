<script>
// import ContentFeed from './ContentFeed.vue'
import LeftNavbar from "./components/LeftNavbar.vue";
import RightNavbar from "./components/RightNavbar.vue";
// import StoryCarousel from './StoryCarousel.vue'
import TopNavbar from "./components/TopNavbar.vue";

export default {
  name: "App",
  components: {
    TopNavbar,
    // ContentFeed,
    LeftNavbar,
    RightNavbar,
    // StoryCarousel,
  },
};
</script>

<template>
  <TopNavbar />
  <div id="app">
    <header>
      <h1>Facebook</h1>
    </header>
    <main>
      <LeftNavbar />
      <section class="news-feed">
        <h2>News Feed</h2>
        <!-- Add more content to mimic the Facebook homepage -->
        <ContentFeed />

        <RightNavbar />
        <StoryCarousel />
      </section>
    </main>
  </div>
</template>

<style>
#app {
  font-family: "Arial", sans-serif;
  text-align: center;
  color: #1c1e21;
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
