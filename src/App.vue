<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
.debug {
    outline: 2px solid red;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow-x: clip;
}

.sr-only {
    display: none !important;
}

</style>
