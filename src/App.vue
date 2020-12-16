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
                    <p>
                        hello@tdos.nz
                        +64 (0) 123 4567
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
		padding-left: 100px;
		padding-top:10px
	}
	#nav {
		display: block;
	}
	header {
		z-index: 100;
		height: 40px;
		margin: 0px 20px;
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
		z-index: 100;
		height:200px;
		margin:0px 30px;

		overflow:hidden;
		border-top:solid 2px;
	}
	.footer-column-1{
		float:left;
		width:10%;
		border-right:solid 0px;
		font-weight:500;
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
	.footer-title{
		padding-top:30px;
		font-weight:600;
		font-style:normal;
		letter-spacing:1px;
		font-size:20px;
		color:#ffffff;
	}
	.footer-column-1 p{
		padding-top:10px;
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
