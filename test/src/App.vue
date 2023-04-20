<template>
  <div id="app">
    <BaseHeader />
    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue';
export default {
  components: {
    BaseHeader
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

div,
header,
footer,
ul,
li,
main {
  display: flex;
}
main{
  flex-direction: column;
  align-items: center;
}
.container {
  width: 100%;
  max-width: 1600px;
}

#app {
  display: flex;
  flex-direction: column;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  width: 100%;
  height: 100%;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
