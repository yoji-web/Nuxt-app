<template>
  <section class="container">
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
    <hr>
    <router-link to="/other">Go to Other</router-link>
  </section>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'hello',
      message: 'This is message.',
      now: 'wait..',
    };
  },
  created: function() {
    setInterval(() => {
      var d = new Date();
      this.now = d.getHours()
        + ':' + d.getMinutes()
        + ':' + d.getSeconds();
    }, 2000);
  },
};
</script>

<style>
.container {
  padding: 5px 10px;
  /*margin: 0 auto;*/
  /*min-height: 100vh;*/
  /*display: flex;*/
  /*justify-content: center;*/
  /*align-items: center;*/
  /*text-align: center;*/
}
h1 {
  font-size: 60pt;
  color: #345980;
}
p {
  padding-top: 5px;
  font-size: 20pt;
}
pre {
  padding: 10px;
  font-size: 18pt;
  background-color: #efefef;
}
hr {
  margin: 10px 0px;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
