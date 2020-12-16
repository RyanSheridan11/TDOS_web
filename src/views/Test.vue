<template>
    <div class="test">
			<Particles
			id="tsparticles"
				:options="{
					fpsLimit: 60,
					interactivity: {
						detectsOn: 'canvas',
						events: {
							onClick: {
								enable: true,
								mode: 'push'
							},
							onHover: {
								enable: true,
								mode: 'bubble'
							},
							resize: true
						},
						modes: {
							bubble: {
								distance: 400,
								duration: 2,
								opacity: 1,
								size: 150,
								speed: 3
							},
							push: {
								quantity: 4
							},
							remove: {
								quantity: 4
							}
						}
					},
					particles: {
						number: {
							value: 80,
							density: {
								enable: true,
								value_area: 800
							},
						},
						color: {
							value: '#000000'
						},
						shape: {
							type: 'circle',
							stroke: {
								width: 0,
								color: '#000000'
							},
							polygon: {
								nb_sides: 5
							},
							image: {
								src: '@/assets/table.jpg',
								width: 100,
								height: 100
							}
						},
						opacity: {
							value: 0.7,
							random: true,
							anim: {
								enable: true,
								speed: 1,
								opacity_min: 0.1,
								sync: false
							}
						},
						size: {
							value: 100,
							random: true,
							anim: {
								enable: true,
								speed: 40,
								size_min: 0.1,
								sync: false
							}
						},
						line_linked: {
							enable: false,
							distance: 150,
							color: '#ffffff',
							opacity: 1,
							width: 1
						},
						move: {
							enable: true,
							speed: 2,
							direction: 'none',
							random: false,
							straight: false,
							outMode: 'out',
							attract: {
								enable: false,
								rotateX: 600,
								rotateY: 1200
							}
						},


					},
					backgroundMask: {
						enable: true,
						cover: {
							color: {
								value: '#2f4454'
							}
						}
					},
					background: {
						image: 'url(assets/table.jpg)'
					},

					detectRetina: true
				}"/>
			<img id="background-pic" alt="Our first table" src="@/assets/table.jpg">

			<div id="menuToggle">
				<input type="checkbox" />

				<span></span>
				<span></span>
				<span></span>
				<ul id="menu">
					<a href="#"><li>Home</li></a>
					<a href="#"><li>About</li></a>
					<a href="#"><li>Info</li></a>
					<a href="#"><li>Contact</li></a>
				</ul>
			</div>

    </div>
</template>

<style>
	#menuToggle	{
		display: block;
		position: fixed;
		top: 40px;
		right: 50px;
		z-index: 2;
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
		left: -5px;
		cursor: pointer;

		opacity: 0; /* hide this */
		z-index: 3; /* and place it over the hamburger */

		-webkit-touch-callout: none;
	}

	#menuToggle span {
		display: block;
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
		margin: -100px 0 0 -50px;
		padding: 50px;
		padding-top: 125px;

		background: #ededed;
		list-style-type: none;
		-webkit-font-smoothing: antialiased;
		/* to stop flickering of text in safari */

		transform-origin: 0% 0%;
		transform: translate(100%, 0);

		transition: transform 0.5s cubic-bezier(0.77,0.2,0.05,1.0);
	}
	#menu li {
		padding: 10px 0;
		font-size: 22px;
	}
	#menuToggle input:checked ~ ul {
		transform: none;
	}
	#tsparticles {
		visibility: hidden;
		z-index: -1;
		position: fixed;
		left: 0;
		top: 0;
		width: 100vw;
		height: 100vh;

		background-repeat: no-repeat;
		background-size: cover;
		background-position: 50% 50%;
	}
	#background-pic {
		position: fixed;
		left: 0;
		top: 0;
		width: 100vw;
		height: 100vh;
		z-index: -2;
	}
	footer, header {
		visibility: hidden;
	}
</style>
