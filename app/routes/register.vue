<template lang="html">
  <div class="register">
    <div class="section">
      <div class="container">
        <div class="card">
          <div class="card__header">
            <h1 class="card__header-title">Create an Account</h1>
          </div>

          <div class="card__body">
            <p class="label">Username</p>
            <input type="text" class="input" placeholder="Username">
            <p class="label">E-mail</p>
            <input type="text" class="input" placeholder="E-mail">
            <p class="label">Password</p>
            <input type="text" class="input" placeholder="Password">
          </div>

          <div class="card__footer">
            <router-link :to="{ name: 'login' }"><button class="button button-blue">Login</button></router-link>
            <!-- fix route -->
            <router-link :to="{ name: 'login' }"><button class="button button-green">Sign up</button></router-link>
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
