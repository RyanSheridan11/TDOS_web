<template>
    <header>
        <router-link class="nav-link" :to="{name: 'Home'}"><img id="site-logo" src="@/assets/tdos_logo.png" /></router-link>
        <div class="header-section-right">
            <router-link class="nav-link" :to="{ name: 'Home'}">projects</router-link> .
            <router-link class="nav-link" :to="{ name: 'About'}"> about</router-link> .
            <router-link class="nav-link" :to="{ name: 'Store'}">store</router-link> .
            <router-link class="nav-link" :to="{ name: 'Test'}">test</router-link>
        </div>
    </header>
    <router-view />
    <footer class="site-footer">
        <div class="container">
            <div class="row">
                <div class="footer-column-1">
                    <div class="footer-title">
                        <router-link class="nav-link" id="footer-title-text" to="{name: 'Contact'}">Contact_</router-link>
                    </div>
                    <p class="footer-text">

                        hello@tdos.nz
                        </p>
                    <p class="footer-text">
                        +64 (0) 123 4567
                        </p>
                    <p class="footer-text">
                        aro valley, wellington
                    </p>
                </div>
                <div class="footer-column-2">

                </div>
            </div>
        </div>
    </footer>
</template>

<style>

#app {
  font-family: "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
}
html{ 
    scroll-behavior: smooth;
}
body{
    margin:0;
    padding:0;
    background:#2f4454;
}
main {
    
    height: 100%;
    width: 100%;
    background:#2f4454;
}
#site-logo {
    width: 100px; 
    height: auto; 
    float: left; 
    padding-left: 50px;
    padding-top:10px
}

#nav {
    display: block;
}
header {
    height: 60px;
    margin: 0px 10px;
    border-bottom: solid 2px;
    
}
header p:hover{
    color:rgba(0,0,0,.5);
}
header .nav-link{
    text-decoration:none;
    color:#ffffff;
}

    
 .header-section-left{
 }

 .header-section-right{
     font-weight: 300;
     font-style: normal;
     letter-spacing: 1px;
     float: right;
     padding-top:30px;
     font-size:20px;
     text-decoration:none;
     color:#da7b93;
     padding-right:50px;
     
 }

 footer{
     height:200px;
     margin:0px 10px;
     
     overflow:hidden;
     border-top:solid 2px;
 }
 .footer-column-1{
     float:left;
     width:250px;
     font-weight:500;
     margin-left:30px;
 }
 footer .nav-link {
     padding-top:0px;
        float: left;
        text-align: center;
        line-height: 0px;
        border-radius: 20px;
        text-decoration: none;
        color:#ffffff;
 }
 .footer-text{
     padding-top:0px;
     margin-top:0px;
     margin-bottom:0px;
 }
    .footer-title{
        padding-top:30px;
        font-weight:600;
        font-style:normal;
        letter-spacing:1px;
        font-size:20px;
        color:#ffffff;
        padding-bottom:10px;
        margin-bottom:10px;
    }
    .footer-column-1 p{
        padding-top:0px;
        letter-spacing:1px;

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
