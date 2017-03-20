<template lang="html">
  <div class="users-index">
    <div class="section">
      <div class="users-container">
        <div class="users-header">
          <h1 class="users-header__text">Users</h1>
        </div>
        <div class="grid">
          <div v-for="user in users" class="grid__item">
            <div class="user-card">
              <img src="http://placecera.com/100/100" alt="" class="user-card__pic">

              <div class="user-card__info">
                <h2 class="user-card__name">{{ user.username }}</h2>
                <h4 class="user-card__id">{{ user.email }}</h4>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import userResource from '../resources/user.js';
const findAll = userResource.actionCreators.findAll;
import store from '../store';

export default {
  data() {
    return {
      users: this.$select('users.items'),
    };
  },

  created() {
    store.dispatch(findAll());
  },

  methods: {

  },
};
</script>
