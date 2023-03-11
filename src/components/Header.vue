<template>
	<div class="menu-container">
		<div class="nav">
			<ul>
				<a href="#"><li>Home</li></a>
				<a href="#menu"><li>Menu</li></a>
				<a href="#events"><li>Events</li></a>
				<a href="#aboutus"><li>About Us</li></a>
			</ul>
		</div>
		<div class="login">
			<button>Log in</button>
		</div>
	</div>

	<header class="header-container">
		<div class="logo">
			<p>pizzashop</p>
		</div>
		<!------------------------------------------------->
		<div class="navigation">
			<ul>
				<a href="#"><li :class="{ active: activeTab === 'home' }" @click="activeTab = 'home'">Home</li></a>
				<a href="#menu"><li :class="{ active: activeTab === 'menu' }" @click="activeTab = 'menu'">Menu</li></a>
				<a href="#events"><li :class="{ active: activeTab === 'events' }" @click="activeTab = 'events'">Events</li></a>
				<a href="#aboutus"><li :class="{ active: activeTab === 'about' }" @click="activeTab = 'about'">About Us</li></a>
			</ul>
		</div>
		<!------------------------------------------------->
		<div class="header-btn">
			<div class="login">
				<button>Log in</button>
			</div>
			<div class="store">
				<img src="../assets/img/store.svg" alt="store">
			</div>
			<div class="header-menu" v-on:click="menuBurger">
				<img src="../assets/img/headeer-menu.svg" alt="burger">
			</div>
		</div>
	</header>
</template>

<script>
	export default {
		data() {
			return {
				isPositioned: false,
				activeTab: 'home',
			};
		},

		methods: {
			menuBurger() {
				var container = document.querySelector('.menu-container')
				var links = document.querySelectorAll('.menu-container .nav ul a')
				this.isPositioned = !this.isPositioned;

				for (var i = 0; i < links.length; i++) {
					if (this.isPositioned) {
						container.classList.add("visible-side")
						document.body.style.overflow = 'hidden'
						links[i].removeEventListener('click', this.hideMenu)
						links[i].addEventListener('click', this.hideMenu)
					} else {
						container.classList.remove("visible-side")
						document.body.style.overflow = 'auto'
						links[i].removeEventListener('click', this.hideMenu)
					}
				}
			},

			hideMenu() {
				var container = document.querySelector('.menu-container')
				container.classList.remove("visible-side")
				document.body.style.overflow = 'auto'
				this.isPositioned = false;
			},
		},
	};
</script>

<style scoped lang="scss">
	@import '../assets/vars';
	@import '../assets/extends';

	.menu-container{
		width: 100%;
		height: 100vh;
		padding: 30px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-evenly;
		background-color: rgba(20, 20, 20, 0.904);
		position: absolute;
		z-index: -1;
		opacity: 0;
		transition: opacity 0.4s ease;

		&.visible-side {
			opacity: 1;
			z-index: 10;
		}

		>.nav{
			text-align: center;
			
			>ul{
				font-style: normal;
				font-weight: 400;
				font-size: 17.8805px;
				line-height: 109.5%;
				color: #A3A3A3;

				>a{
					cursor: pointer;
					li{
						margin-bottom: 25px;
						&:hover{
							font-style: normal;
							font-weight: 400;
							font-size: 17.8805px;
							line-height: 109.5%;
							background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
							-webkit-background-clip: text;
							-webkit-text-fill-color: transparent;
							background-clip: text;
						}	
					}
				}
			}
		}

		>.login{
			>button{@extend %allButtons;}
		}
	}

	.header-container{
		padding: 20px 5% 0;
		display: flex;
		justify-content: space-between;
		
		>.logo{
			display: flex;
    		align-items: center;
			font-style: normal;
			font-weight: 800;
			font-size: 23.7564px;
			line-height: 109.5%;
			background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
			-webkit-background-clip: text;
			-webkit-text-fill-color: transparent;
			background-clip: text;
		}

		>.navigation{display: none;}

		>.header-btn{
			display: flex;
			align-items: center;
			justify-content: flex-end;

			>.login{display: none;}
			
			>.store, .header-menu{
				display: flex;
				align-items: center;
				cursor: pointer;
			}

			>.store{margin-right: 20px;}

			>.header-menu{
				position: relative;
				z-index: 12;
			}

			>.header-menu:hover,
			>.store:hover{opacity: 0.7;}
		}
	}

	@media screen and (min-width: 1000px){
		.menu-container{display: none;}

		.header-container{
			>.logo{font-size: 34.0578px;}

			>.navigation{
				display: flex;
				align-items: center;

				>ul{
					display: flex;
					font-style: normal;
					font-weight: 400;
					font-size: 17.8805px;
					line-height: 109.5%;
					color: #A3A3A3;
					
					a:not(:last-of-type){margin-right: 60px;}

					li:hover{
						background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
						-webkit-background-clip: text;
						-webkit-text-fill-color: transparent;
						background-clip: text;
					}

					li{
						&:hover{
							font-style: normal;
							font-weight: 400;
							font-size: 17.8805px;
							line-height: 109.5%;
							background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
							-webkit-background-clip: text;
							-webkit-text-fill-color: transparent;
							background-clip: text;
						}	

						&.active{
							background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
							-webkit-background-clip: text;
							-webkit-text-fill-color: transparent;
							background-clip: text;
							position: relative;

							&::before{
								content: "";
								pointer-events: none;
								position: absolute;
								width: 7px;
								height: 7px;
								background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
								border-radius: 50%;
								bottom: -13px;
								left: 45%;
							}
						}
					}
				}
			}

			>.header-btn{
				>.login{
					display: block;
					margin-right: 30px;
					>button{
						font-style: normal;
						font-weight: 500;
						font-size: 17.74px;
						line-height: 109.5%;
						color: #FFFFFF;
						width: 145px;
						padding: 12px;
						background: linear-gradient(261.69deg, #FF5D29 12.12%, #FE9C1C 86.72%);
						border-radius: 30px;
						cursor: pointer;
						transition: transform 0.5s ease;
						&:hover{opacity: 0.7;}
					}
				}

				>.store{margin-right: 0;}
				>.header-menu{display: none;}
			}
		}
	}

	@media screen and (min-width: 1400px){
		.header-container{
			>.navigation{
				>ul{
					>a:not(:last-of-type){margin-right: 100px;}
				}
			}
		}
	}

	@media (min-width: 1440px){
		.header-container {
			max-width: 1440px;
			margin: 0 auto;
		}
	}
</style>
