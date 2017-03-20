<template lang="html">
  <!-- v-if="error" @click="error = false" -->
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
    save() {
      fetch('http://localhost:3333/login', {
        method: 'POST',
        headers: { Accept: 'application/json', 'Content-Type': 'application/json' },
        body: JSON.stringify(this.formValues)
      }).then((res) => {
        if (res.ok) {
          return res.json();
        }

        return Promise.reject(res.json());
      }).then((data) => {
        localStorage.jwt = data.token;
      }).catch((error) => {
        this.error = true;
      });
    }

  }
};
</script>
