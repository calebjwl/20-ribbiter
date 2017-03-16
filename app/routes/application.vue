<template lang="html">
  <div class="application">
    <div class="top-nav">
      <div class="home">
        <a href="#">Ribbiter</a>
      </div>

      <div class="top-nav_links">
        <a href="#" class="link">Ribbets</a>
        <a href="#" class="link">Frogs</a>
        <a href="#" class="link">Login</a>
      </div>
    </div>

    <router-view></router-view>
  </div>
</template>

<script>
export default {
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
