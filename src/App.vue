<template>
    <header>
            <router-link class="nav-link" :to="{name: 'Home'}"><img id="site-logo" src="@/assets/tdos_logo.png" /></router-link>
            <div class="header-section-right">
                <router-link class="nav-link" :to="{ name: 'Home'}">Projects</router-link> |
                <router-link class="nav-link" :to="{ name: 'About'}"> About</router-link> |
                <router-link class="nav-link" :to="{ name: 'Store'}">Store</router-link> |
                <router-link class="nav-link" :to="{ name: 'Test'}">Test</router-link>
            </div>
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
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #333;
}
html{ 
    scroll-behavior: smooth;
}
main {
    padding-top:0px;
    height: 100%;
    width: 100%;
}
#site-logo {
    width: 60px; 
    height: auto; 
    float: left; 
    padding-left: 0px;
}

#nav {
    display: block;
}
header {
    height: 37px;
    margin: 0px 30px;
    background-color: #fafafa;
}
    
 .header-section-left{
 }

 .header-section-right{
     font-weight: 300;
     font-style: normal;
     letter-spacing: 1px;
     float: right;
 }
    /*
    #nav a {
        font-weight: bold;
        color: #2c3e50;
        }-->

        <!--#nav a.router-link-exact-active {
        color: #42b983;
        }-->
    */
</style>
