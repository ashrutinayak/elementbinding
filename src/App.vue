<template>
  <div id="app">
    <label for="name">Name</label>
    <br />
    <input type="text" v-model.lazy="name" />
    <br />
    <label for="email">Email</label>
    <br />
    <input type="email" v-model.lazy="email" />
    <div id="checkbox">
      <label for="ReadingNovel">ReadingNovel</label>
      <input type="checkbox" value="ReadingNovel" v-model.lazy="hobbies" />
      <label for="Play Kho-kho">Play Kho-kho</label>
      <input type="checkbox" value="Play Kho-kho" v-model.lazy="hobbies" />
      <label for="Travelling">Travelling</label>
      <input type="checkbox" value="Travelling" v-model.lazy="hobbies" />
      <label for="WatchingMovie">Watching Movie</label>
      <input type="checkbox" value="Watching Movie" v-model.lazy="hobbies" />
    </div>
    <div id="review">
      <label for="Readname">UserName: {{ name }}</label>
      <br />
      <label for="Reademail">UserEmail: {{ email }}</label>
      <br />
      <label for="Reademail">User Hobbies:</label>
      <ul>
        <li v-for="hobby in hobbies" v-bind:key="hobby">{{ hobby }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      hobbies: []
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
label {
  margin: 20px;
  text-align: left;
}
#review {
  margin: 50px;
}
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
