<template>
<<<<<<< HEAD
  <div class="top-nav">
    <div class="logo">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg"
        alt="Facebook Logo"
      />
    </div>
    <div class="search-bar">
      <input type="text" placeholder="Search Facebook" />
      <i class="fas fa-search"></i>
    </div>
    <div class="nav-links">
      <a href="#">Home</a>
      <a href="#">Friends</a>
      <a href="#">Messages</a>
    </div>
    <div class="user-profile">
      <img src="https://via.placeholder.com/150" alt="User Profile" />
      <span>John Doe</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "FacebookTopNav",
};
</script>

<style scoped>
.top-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #3b5998;
  color: white;
  padding: 10px 20px;
}

.logo img {
  height: 40px;
}

.search-bar {
  margin: 0 20px;
  /* position: relative; */
  width: 500px;
}

.search-bar input {
  width: 100%;
  padding: 8px 30px 8px 10px;
  border-radius: 20px;
  border: none;
  background-color: #ffffff;
  color: #3b5998;
}

.search-bar i {
  position: absolute;
  right: 10px;
  top: 50%;
  transform: translateY(-50%);
}

.nav-links a {
  margin-right: 20px;
  color: white;
  text-decoration: none;
}

.user-profile img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
}

.user-profile span {
  font-weight: bold;
}
</style>
=======
>>>>>>> 0246eafd35eac976279ee7f0ef4130409a9406df
