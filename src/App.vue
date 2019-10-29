<template>
  <div id="app">
    <Header></Header>
    <Search @searchKey='searchKey'></Search>
    <ServerList></ServerList>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Search from "./components/Search.vue";
import ServerList from "./components/ServerList.vue";
export default {
  name: "app",
  components: {
    Search,
    Header,
    ServerList
  },
  methods: {
    searchKey: function(val) {
      console.log(val);
    }
  }
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
}
html,
body {
  font: 12px/22px "微软雅黑", "\5b8b\4f53", Arial, sans-serif;
  color: #666;
}
button,
input,
select,
textarea {
  font-family: inherit;
  font-size: 100%;
  margin: 0;
  outline: none;
}
ul,
ol,
li {
  list-style: none;
}
a {
  text-decoration: none;
  background: transparent;
  outline: none;
}
</style>