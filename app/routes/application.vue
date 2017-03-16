<template lang="html">
  <div class="application">
    <div class="top-nav">
      <div class="home">
        <router-link class="link" :to="{ name: 'ribbits' }">Ribbiter</router-link>
      </div>

      <div class="top-nav_links">
        <router-link class="link" :to="{ name: 'ribbits' }">Ribbits</router-link>
        <router-link class="link" :to="{ name: 'frogs' }">Frogs</router-link>
        <router-link class="link" :to="{ name: 'login' }">Login</router-link>
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
