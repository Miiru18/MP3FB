<template>
  <div class="story-carousel">
    <div class="arrow left-arrow" @click="scrollCarousel(-1)">&#10094;</div>
    <div class="carousel-container">
      <div class="carousel-item" v-for="(story, index) in stories" :key="index" style="position: relative;">
        <img class="carousel-item-img" :src="story.image" :alt="story.altText" v-if="!story.isAddStory" />
        <div class="story-name" v-if="!story.isAddStory">{{ story.name }}</div>
        <div class="add-story-card" v-if="story.isAddStory">
          <div class="add-story-icon">+</div>
          <div class="add-story-text">Create Story</div>
        </div>
      </div>
    </div>
    <div class="arrow right-arrow" @click="scrollCarousel(1)">&#10095;</div>
  </div>
</template>

<script>
export default {
  name: "StoryCarousel",
  data() {
    return {
      stories: [
        { image: "../../images/luis.jpg", altText: "Add Story", name: "Add Story", isAddStory: true },
        { image: "../../images/bai.jpg", altText: "Story 1", name: "Diego Jumagdao" },
        { image: "../../images/vff.jpg", altText: "Story 2", name: "Aimee Soriano" },
        { image: "../../images/johnny.jpg", altText: "Story 3", name: "John Cena" },
      ],
      currentIndex: 0,
    };
  },
  methods: {
    scrollCarousel(direction) {
      const container = this.$el.querySelector('.carousel-container');
      const width = container.offsetWidth;
      const maxScroll = container.scrollWidth - width;
      if (direction === -1 && this.currentIndex > 0) {
        this.currentIndex--;
      } else if (direction === 1 && this.currentIndex < this.stories.length - 1) {
        this.currentIndex++;
      }
      container.scrollLeft = this.currentIndex * width;
    }
  }
};
</script>

<style scoped>
.story-carousel {
  display: flex;
  align-items: center;
  margin-top: 30px;
  position: relative;
}

.carousel-container {
  display: flex;
  overflow-x: hidden;
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
}

.carousel-item {
  flex: 0 0 auto;
  margin-right: 10px;
  scroll-snap-align: start;
  width: 200px;
  position: relative;
}

.carousel-item-img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  filter: blur(3px);
}

.story-name {
  position: absolute;
  bottom: 0;
  left: 0;
  padding: 5px;
  color: white;
  font-size: 14px;
}

.add-story-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background-color: #f0f0f0;
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
}

.add-story-icon {
  font-size: 30px;
  color: #007bff;
}

.add-story-text {
  font-size: 14px;
  color: #333;
}

.arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 24px;
  cursor: pointer;
  color: white; /* Set arrow color to white */
  z-index: 1; /* Ensure the arrows are on top of other elements */
}

/* Left arrow */
.left-arrow {
  left: 10px;
}

/* Right arrow */
.right-arrow {
  right: 10px;
}
</style>