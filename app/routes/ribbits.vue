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

              <div class="card__body">
                <h4 class="label">What's hoppin?</h4>
                <textarea class="textbox" id="" cols="40" rows="8"></textarea>
              </div>

              <div class="card__footer">
                <button class="button button-blue">Clear</button>
                <button class="button button-green">Save</button>
              </div>
            </div>
          </div>

          <div class="feed">
            <div class="card shadow">
              <div class="card__header">
                <h3 class="card__header-title">See What's Hoppin'</h3>
              </div>

              <div class="card__body">
                <button class="button button-blue feed-load">
                  <h3 class="feed-load__text">Load New Ribbits</h3>
                </button>
              </div>

              <div class="panel">
                <h3 class="user-card__id">$caleb</h3>
                <p>This is a ribbit</p>
              </div>
            </div>
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
