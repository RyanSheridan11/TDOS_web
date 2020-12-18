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
							value: 250,
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
				}"
			/>
			<img id="background-pic" alt="Our first table" :src="imageSrc">


    </div>
</template>

<script>
  // @ is an alias to /src
  //import HelloWorld from '@/components/HelloWorld.vue'
  export default {
    name: 'Test',
    components: {
        //HelloWorld
    },
		computed: {
			tableImages () {
				return require("../assets/tables/" + this.images[Math.abs(this.currentImage) % this.images.length])
			}
		},
		data () {
			return {
				images: ["table.jpg", "table2.jpg","table3.jpg"],
				currentImage: 0,
				timer: null,
				imageSrc: this.tableImages,
			}
		},
		mounted: function () {
			this.startRotation();
		},
		methods: {
			startRotation: function() {
				this.timer = setInterval(this.next, 2000); //This is the timer to rotate images, increase/decrease as you like
			},  //5000 = 5 seconds
			next: function () {
				this.currrentImage +=1
				this.imageSrc = this.tableImages
			},
			prev: function () {
				this.currentImage -=1
			}
		},

  }
</script>

<style>
	#tsparticles {
		z-index: 2;
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
		z-index: 1;
	}
</style>
