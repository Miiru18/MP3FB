<template>
 <div class="story-carousel">
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
    };
 },
};
</script>

<style scoped>
.story-carousel {
 display: flex;
 justify-content: center;
 margin-top: 30px; /* Adjust as needed to position below the top navbar */
}

.carousel-container {
 display: flex;
 overflow-x: auto;
 scroll-snap-type: x mandatory;
 -webkit-overflow-scrolling: touch;
}

.carousel-item {
 flex: 0 0 auto;
 margin-right: 10px;
 scroll-snap-align: start;
 width: 200px; /* Adjust the width as needed */
 position: relative; /* Important for absolute positioning of the story name and add story card */
}

.carousel-item-img {
 width: 100%;
 height: 250px; /* Set a fixed height for the image */
 object-fit: cover; /* Ensure the image covers the area without stretching */
 filter: blur(3px); /* Add blur effect to the images */
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
 background-color: #f0f0f0; /* Light grey background */
 position: absolute;
 bottom: 0;
 left: 0;
 right: 0;
}

.add-story-icon {
 font-size: 30px;
 color: #007bff; /* Blue color */
}

.add-story-text {
 font-size: 14px;
 color: #333; /* Dark grey text */
}

.carousel-container::-webkit-scrollbar {
 display: none;
}
</style>
