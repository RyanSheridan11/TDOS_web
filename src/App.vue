<template>
    <header id="nav">
        <router-link :to="{ name: 'Home'}">TDOS</router-link> |
        <router-link :to="{ name: 'Home'}" >Projects</router-link> |
        <router-link :to="{ name: 'About'}"> About</router-link> |
        <router-link :to="{ name: 'Store'}">Store</router-link>
    </header>
    <router-view />
    <footer class="site-footer">
        <router-link :to="{ name: 'Contact'}" tag="h3">Contact_</router-link>
        <h5>hello@tdos.nz</h5>
        <h5>+64 (0) 123 4567</h5>
        <h5>aro valley, wellington</h5>
    </footer>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
