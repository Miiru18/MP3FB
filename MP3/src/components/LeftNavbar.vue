<template>
<<<<<<< HEAD
  <div class="left-navbar">
    <ul>
      <li><a href="#">Profile</a></li>
      <li><a href="#">Friends</a></li>
      <li><a href="#">Photos</a></li>
      <!-- Add more items as needed -->
    </ul>
  </div>
</template>

<script>
export default {
  name: "LeftNavbar",
};
</script>

<style scoped>
.left-navbar {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%; /* Make the navbar full height */
  width: 200px; /* Adjust the width as needed */
  background-color: #4267b2;
  padding: 10px;
  margin-top: 170px;
  margin-left: 8px;
}

.left-navbar ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.left-navbar li {
  margin-bottom: 8px;
}

.left-navbar a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
}

.left-navbar a:hover {
  color: #4267b2; /* Facebook blue */
}
</style>
