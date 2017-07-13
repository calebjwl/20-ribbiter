<template lang="html">
  <div class="index">
    <h1 class="welcome">Welcome to Ribbiter!</h1>
    <div class="button-list">
      <router-link :to="{ name: 'login' }"><button class="button">Login</button></router-link>
      <router-link :to="{ name: 'register' }"><button class="button">Register</button></router-link>
    </div>
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
