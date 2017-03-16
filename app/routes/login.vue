<template lang="html">
  <div class="login">
    <div class="section">
      <div class="container">
        <div class="card">
          <div class="card__header">
            <h1 class="card__header-title">Login</h1>
          </div>

          <div class="card__body">
            <p class="label">E-mail</p>
            <input type="text" class="input" placeholder="E-mail">
            <p class="label">Password</p>
            <input type="text" class="input" placeholder="Password">
          </div>

          <div class="card__footer">
            <router-link :to="{ name: 'register' }"><button class="button button-blue">Register</button></router-link>
            <!-- fix route -->
            <router-link :to="{ name: 'login' }"><button class="button button-green">Login</button></router-link>
          </div>
        </div>
      </div>
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
