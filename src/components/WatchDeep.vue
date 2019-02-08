<template>
  <div class="hello">
    <ul>
      <li v-for="color in colors">{{ color.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "WatchDeep",
  data() {
    return {
      colors: [{ name: "Red" }, { name: "White" }, { name: "Blue" }]
    };
  },
  watch: {
    colors: {
      handler: function(newValue, oldValue) {
        console.log("Update!");
        console.log(
          "new: %s, old: %s ",
          JSON.stringfy(newValue, null, "\t"),
          JSON.stringfy(oldValue, null, "\t")
        );
      },
      deep: true
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
