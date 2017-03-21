<template lang="html">
  <div class="ribbits">
    <div class="section">
      <div class="users-container">
        <div class="users-header">
          <h1 class="users-header__text">Ribbits</h1>
        </div>

        <div class="ribbits-container">
          <div class="sidebar">
            <div class="card shadow">
              <div class="card__header">
                <h3 class="card__header-title">New Ribbit</h3>
              </div>

              <form class="card__body" v-on:submit.prevent="save()">
                <h4 class="label">What's hoppin?</h4>
                <textarea v-model="formValues.body" class="textbox" id="" cols="40" rows="8"></textarea>
                <div class="card__footer">
                  <button v-on:click.prevent="clear()" class="button button-blue">Clear</button>
                  <button class="button button-green">Post</button>
                </div>
              </form>
            </div>
          </div>

          <div class="feed">
            <div class="card shadow">
              <div class="card__header">
                <h3 class="card__header-title">See What's Hoppin'</h3>
              </div>

              <div class="card__body">
                <button v-on:click = "loadNew()" class="button button-blue feed-load">
                  <h3 class="feed-load__text">Load New Ribbits</h3>
                </button>
              </div>

              <div class="posts" v-for="post in posts.items">
                <div class="panel">
                  <h3 class="user-card__id">{{ post.username }}</h3>
                  <p>{{ post.body }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import postResource from '../resources/post';
import userResource from '../resources/user';
import store from '../store';
const findAll = postResource.actionCreators.findAll;
const create = userResource.actionCreators.create;

export default {
  data() {
    return {
      posts: this.$select('posts'),
      formValues: {
        body: '',
      }
    };
  },

  created() {
    store.dispatch(findAll());
  },

  methods: {
    save() {
      store.dispatch(create(this.formValues));
      this.formValues.body = '';
    },

    clear() {
      this.formValues.body = '';
    },

    loadNew() {
      store.dispatch(findAll());
    }
  },
};
</script>
