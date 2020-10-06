<template>
  <nav class="navbar">
    <div class="container">
      <div class="navbar-brand">
        <a class="navbar-item navbar-image">
        </a>
      </div>
      <div class="navbar-menu">
        <div class="navbar-end">
          <a class="navbar-item has-text-grey-dark"> 1Jam on Itch.io </a>

        </div>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  name: "NavBar",

};
</script>

<style scoped>
.navbar-image {
  background: url('../assets/1jam.png') no-repeat
    center center;
  background-size: cover;
  width: 110px;
}
</style>