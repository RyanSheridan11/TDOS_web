<template>
    <header>
			<div id="">
				<router-link class="nav-link" :to="{name: 'Home'}"><img id="site-logo" src="@/assets/tdos_logo.png" /></router-link>
			</div>
			<div id="menuToggle">
				<input type="checkbox" />
				<span></span>
				<span></span>
				<span></span>
				<ul id="menu">
					<li> <router-link class="nav-link" :to="{ name: 'Home'}">projects</router-link> . <router-link class="nav-link" :to="{ name: 'About'}"> about</router-link> . <router-link class="nav-link" :to="{ name: 'Store'}">store</router-link> . <router-link class="nav-link" :to="{ name: 'Test'}">test</router-link></li>
				</ul>
			</div>
    </header>
    <router-view />
    <footer class="site-footer">
        <div class="container">
            <div class="row">
                <div class="footer-column-1">
                    <div class="footer-title">
                        <router-link class="nav-link" id="footer-title-text" :to="{ name: 'Contact'}">Contact_</router-link>
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
	header {
		height: 80px;
		z-index: 4;
	}
	html{
		scroll-behavior: smooth;
	}
	body {
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
		z-index: 4;
		position: absolute;
		width: 100px;
		height: auto;
		float: left;
		padding-left: 50px;
		padding-top:10px
	}
	#nav {
		display: block;
	}
	#menuToggle	{
		display: block;
		position: fixed;
		top: 40px;
		right: 50px;
		z-index: 3;
		-webkit-user-select: none;
		user-select: none;
	}
	#menuToggle a	{
		text-decoration: none;
		color: #232323;
		transition: color 0.3s ease;
	}
	#menuToggle a:hover	{
		color: tomato;
	}
	#menuToggle input	{
		display: block;
		width: 40px;
		height: 32px;
		position: absolute;
		top: -7px;
		/* left: -5px; */
		right: -30px;
		cursor: pointer;

		opacity: 0; /* hide this */
		z-index: 4; /* and place it over the hamburger */
		-webkit-touch-callout: none;
	}

	#menuToggle span {
		display: block;
		right: -25px;
		width: 33px;
		height: 4px;
		margin-bottom: 5px;
		position: relative;
		background: #cdcdcd;
		border-radius: 3px;
		z-index: 2;
		transform-origin: 4px 0px;
		transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
		background 0.5s cubic-bezier(0.77,0.2,0.05,1.0),
		opacity 0.55s ease;
	}
	#menuToggle span:first-child {
		transform-origin: 0% 0%;
	}
	#menuToggle span:nth-last-child(2) {
		transform-origin: 0% 100%;
	}
	#menuToggle input:checked ~ span {
		opacity: 1;
		transform: rotate(45deg) translate(-2px, -1px);
		background: #232323;
	}
	#menuToggle input:checked ~ span:nth-last-child(3) {
		opacity: 0;
		transform: rotate(0deg) scale(0.2, 0.2);
	}
	#menuToggle input:checked ~ span:nth-last-child(2) {
		transform: rotate(-45deg) translate(0, -1px);
	}
	#menu {
		position: absolute;
		width: 300px;
		margin: -53px 0 0 0;
		padding: 10px;

		list-style-type: none;
		-webkit-font-smoothing: antialiased;
		/* to stop flickering of text in safari */

		transform-origin: 0% 0%;
		right: -20px;
		transform: translate(120%, 0);

		transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0);
	}
	#menu li {
		padding: 10px 0;
		font-size: 22px;
	}
	#menuToggle input:checked ~ ul {
		transform: none;
	}
	footer {
		height:200px;
		margin:0px 10px;

		overflow:hidden;
		border-top:solid 2px;
	}
	.footer-column-1 {
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
	.footer-text {
		padding-top:0px;
		margin-top:0px;
		margin-bottom:0px;
	}
	.footer-title {
		padding-top:30px;
		font-weight:600;
		font-style:normal;
		letter-spacing:1px;
		font-size:20px;
		color:#ffffff;
		padding-bottom:10px;
		margin-bottom:10px;
	}
	.footer-column-1 p {
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
