<template lang="html">
  <div class="register">
    <div class="section">
      <div class="container">
        <div class="error" v-if="users.loading === 'error'">
          <h2 class="error-text">There was an error. Please try again.</h2>
        </div>
        <div class="card">
          <div class="card__header">
            <h1 class="card__header-title">Create an Account</h1>
          </div>

          <div class="card__body">
            <p class="label">Username</p>
            <input type="text" class="input" placeholder="Username" v-model="formValues.username">
            <p class="label">E-mail</p>
            <input type="text" class="input" placeholder="E-mail" v-model="formValues.email">
            <p class="label">Password</p>
            <input type="text" class="input" placeholder="Password" v-model="formValues.password">
          </div>

          <div class="card__footer">
            <router-link :to="{ name: 'login' }"><button class="button button-blue">Login</button></router-link>
            <button v-on:click="save()" class="button button-green">Sign up</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import userResource from '../resources/user.js';
import store from '../store';
const create = userResource.actionCreators.create;

export default {
  data() {
    return {
      users: this.$select('users'),
      formValues: {
        username: '',
        email: '',
        password: '',
      }
    };
  },

  methods: {
    save() {
      store.dispatch(create(this.formValues))
      .then(() => {
        this.$router.push({ name: 'frogs' });
      }).catch(() => {});
    },

  },
};
</script>
