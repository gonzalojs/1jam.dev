<template>
  <section class="hero is-primary is-fullheight">
    <!-- Hero head: will stick at the top -->
    <div class="hero-head">
      <NavBar />
    </div>

    <!-- Hero content: will be in the middle -->
    <div class="hero-body">
      <div class="container has-text-centered">
        <h1 class="title is-1 has-text-grey-dark">
          <a
            href="https://twitter.com/search?q=%231JAM&src=trend_click&vertical=trends"
            >#1JAM</a
          >
        </h1>
        <h1 class="title is-1 has-text-grey-dark">One Jam A Month</h1>
        <h2 class="subtitle has-text-danger">
          <Counter />
        </h2>
      </div>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
/* import HelloWorld from '@/components/HelloWorld.vue' */
import NavBar from "@/components/NavBar.vue";
import Counter from "@/components/Counter.vue";

export default {
  name: "Home",
  components: {
    NavBar,
    Counter,
  },
};
</script>
