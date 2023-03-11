<template>
	<section class="menu-wrapper" id="menu">
		<div class="title">
			<p>Menu</p>
		</div>

		<div class="content-menu">
			<div class="choose-btns">
				<div>
					<button :class="{ activebtn: activeTab === 'show' }" @click="activeTab = 'show'">Show All</button>
				</div>
				<div>
					<button :class="{ activebtn: activeTab === 'meat' }" @click="activeTab = 'meat'">Meat</button>
				</div>
				<div>
					<button :class="{ activebtn: activeTab === 'vegan' }" @click="activeTab = 'vegan'">Vegetarian</button>
				</div>
				<div>
					<button :class="{ activebtn: activeTab === 'prod' }" @click="activeTab = 'prod'">Sea products</button>
				</div>
				<div>
					<button :class="{ activebtn: activeTab === 'mush' }" @click="activeTab = 'mush'">Mushroom</button>
				</div>
			</div>

			<!---------------------------------------->
			<div class="pizza">
				<!---1--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/italian.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Italian</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>8,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>

				<!---2--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/venecia.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Venecia</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>7,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>

				<!---3--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/meat.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Meat</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>9,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>

				<!---4--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/cheese.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Cheese</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>8,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>
			</div>

			<!---------------------------------------->
			<div class="most-popular">
				<p>MOST POPULAR PIZZA</p>
			</div>
			<!---------------------------------------->
			<div class="pizza">
				<!---1--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/argentina.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Argentina</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>7,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>

				<!---2--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/gribnaya.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Gribnaya</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>7,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>

				<!---3--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/meat.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Meat</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>9,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>

				<!---4--->
				<div>
					<div class="pizza-img">
						<img src="../assets/img/cheese.png" alt="italian">
					</div>

					<div class="pizza-title">
						<p>Cheese</p>
						<p>Filling: onion, potato, tomato, mushrooms, cheese, olives, meat...</p>
					</div>

					<div class="pizza-size">
						<button class="22" :class="{ default: defaultSize === '22' }" @click="defaultSize = '22'">22</button>
						<button class="28" :class="{ default: defaultSize === '28' }" @click="defaultSize = '28'">28</button>
						<button class="33" :class="{ default: defaultSize === '33' }" @click="defaultSize = '33'">33</button>
					</div>

					<div class="ingridients">
						<button>+ Ingridents</button>
					</div>

					<div class="pizza-set">
						<div class="price">
							<span>8,35</span><sup>$</sup>
						</div>

						<div class="number">
							<button class="minus" v-bind:disabled="disabled">-</button>
							<span>{{ count }}</span>
							<button class="plus" v-bind:disabled="disabled">+</button>
						</div>
					</div>

					<div class="order-now">
						<button>Order Now</button>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
	export default {
		data(){
			return{
				activeTab: 'show',
				defaultSize: '28',
				disabled: false,
				count: 1,
			};
		},

		methods: {
			
		},
	};
</script>

<style scoped lang="scss">
	@import '../assets/vars';
	@import '../assets/extends';

	.menu-wrapper{
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 0 5%;
		margin-bottom: 50px;

		>.title{
			font-style: normal;
			font-weight: 800;
			font-size: 48px;
			line-height: 109.5%;
			color: #FFFFFF;
			margin-bottom: 25px;
		}

		>.content-menu{
			width: 100%;
			display: flex;
			flex-direction: column;
			
			>.choose-btns{
				display: flex;
				flex-wrap: wrap;
				justify-content: space-evenly;
				margin-bottom: 80px;
				
				>div{
					>button{
						@extend %allButtons;
						background: #210A01;
						box-shadow: 0px 5.50332px 24.4592px rgba(255, 107, 0, 0.06);
						&:hover{opacity: 1};
					}

					>button.activebtn{
						@extend %allButtons;
					}
					
					&:first-child,
					&:nth-child(4),
					&:nth-child(5){
						>button{width: 140.6px;}
					}

					&:nth-child(2){
						>button{width: 80px;}
					}

					&:nth-child(3){
						>button{width: 130px;}
					}
				}

				>div:not(:nth-child(4), :nth-child(5)){margin-bottom: 10px;}
			}

			>.pizza{
				display: grid;
				grid-template-columns: repeat(1, 1fr);
				grid-gap: 20px;
				margin-bottom: 50px;
				
				>div{
					padding: 70px 20px 20px;
					background: rgba(33, 10, 1, 1);
					border-radius: 18.0578px;
					position: relative;
					display: flex;
					flex-direction: column;
					align-items: center;

					&:not(:last-of-type){margin-bottom: 60px;}

					>.pizza-img{
						text-align: center;
						height: 140px;
						position: absolute;
						top: -75px;
					
						>img{
							height: inherit;
							filter: drop-shadow(0px 0px 15.287px rgba(255, 138, 0, 0.18));
						}
					}

					>.pizza-title{
						width: 100%;
						text-align: center;
						margin-bottom: 20px;

						>p:first-of-type{
							font-style: normal;
							font-weight: 500;
							font-size: 15.3492px;
							line-height: 109.5%;
							color: #FFFFFF;
							margin-bottom: 11px;
						}

						>p:last-of-type{
							text-align: left;
							font-style: normal;
							font-weight: 400;
							font-size: 8.7562px;
							line-height: 109.5%;
							color: #A3A3A3;
						}
					}

					>.pizza-size{
						margin-bottom: 20px;
						width: 100%;
						display: flex;
						justify-content: space-evenly;

						>button{
							font-style: normal;
							font-weight: 400;
							font-size: 8.7562px;
							line-height: 109.5%;
							color: #A3A3A3;
							@extend %pizzaBtn;
							padding: 10px;
							&:hover{padding: 11px;}

							&.default{
								padding: 11px;
								border: 0;
								color: #FFFFFF;
								background: linear-gradient(261.69deg, #FF5924 12.12%, #FFA229 86.72%);
							}
						}
					}

					>.ingridients{
						margin-bottom: 20px;
						>button{
							font-style: normal;
							font-weight: 400;
							font-size: 10px;
							line-height: 109.5%;
							background: linear-gradient(261.69deg, #FF5924 12.12%, #FFA229 86.72%);
							-webkit-background-clip: text;
							-webkit-text-fill-color: transparent;
							background-clip: text;
							@extend %ingridients;
						}
					}

					>.pizza-set{
						width: 100%;
						display: flex;
						justify-content: space-evenly;
						margin-bottom: 20px;

						>.price{
							font-style: normal;
							font-weight: 500;
							font-size: 15.5654px;
							line-height: 109.5%;
							color: #FFFFFF;
						}

						>.number{
							display: flex;
							align-items: center;
							font-style: normal;
							font-weight: 400;
							font-size: 11px;
							line-height: 109.5%;
							color: #A3A3A3;
							
							>button:first-of-type,
							>span:first-of-type{margin-right: 7px;}

							>span:first-of-type{font-size: 14px;}

							>button{
								width: 20px;
								height: 20px;
								@extend %pizzaBtn;
							}
						}
					}

					>.order-now{
						>button{
							@extend %allButtons;
							width: 120px;
							padding: 10px;
							font-size: 11px;
						}
					}
				}
			}

			>.most-popular{
				width: 100%;
				height: 175px;
				position: relative;
				background: url(../assets/img/slidepizza.png);
				background-size: cover;
				border-radius: 20px;
				display: flex;
				align-items: center;
				justify-content: center;
				margin-bottom: 100px;

				>p:first-of-type{
					font-style: normal;
					font-weight: 500;
					font-size: 27px;
					line-height: 108.5%;
					color: #FFFFFF;
					text-shadow: 0px 7.08737px 6.25356px rgba(14, 4, 4, 0.38);
				}
			}
		}
	}

	@media screen and (min-width: 370px){
		.menu-wrapper{
			>.content-menu{
				>.pizza{
					display: grid;
					grid-template-columns: repeat(2, 1fr);

					>div{
						>.pizza-set{
							display: flex;
							justify-content: space-between;
						}
					}
				}
			}
		}
	}

	@media screen and (min-width: 430px){
		.menu-wrapper{
			>.content-menu{
				>.pizza{
					>div{
						>.pizza-set{
							display: flex;
							justify-content: space-evenly;
						}
					}
				}
			}
		}
	}

	@media screen and (min-width: 730px){
		.menu-wrapper{
			>.content-menu{
				>.pizza{
					display: grid;
					grid-template-columns: repeat(4, 1fr);
					
					>div{
						&:not(:last-of-type){margin-bottom: 0px;}
						>.pizza-set{
							display: flex;
							justify-content: space-between;
						}
					}
				}
			}
		}
	}

	@media screen and (min-width: 1000px){
		.menu-wrapper{
			>.title{font-size: 70px;}
			>.content-menu{
				>.choose-btns{
					>div{
						>button{
							@extend %allButtons;
							width: 200px!important;
							height: 62px;
							font-size: 20px;
						}

						>button.activebtn{
							@extend %allButtons;
							font-size: 20px;
						}
					}

					>div:not(:nth-child(4), :nth-child(5)){margin-bottom: 10px;}
				}
				
				>.pizza{
					>div{
						>.pizza-set{
							display: flex;
							justify-content: space-evenly;
						}

						>.pizza-img{
							height: 150px;
							top: -80px;
						
							>img{
								height: inherit;
								filter: drop-shadow(0px 0px 25px rgba(255, 138, 0, 0.18));
							}
						}
						
						>.pizza-title{
							>p:first-of-type{font-size: 25px;}
							>p:last-of-type{font-size: 14px;}
						}

						>.pizza-size{
							>button{
								font-size: 14px;
								padding: 13px;

								&:hover{padding: 14px;}
								&.default{padding: 14px;}
							}
						}

						>.ingridients{
							>button{
								font-size: 16px;
								padding: 10px 35px!important;
								filter: drop-shadow(0px 7.59366px 33.7496px rgba(255, 107, 0, 0.06))!important;
								border-radius: 85px;
							}
						}

						>.pizza-set{
							>.price{font-size: 25px;}

							>.number{
								font-size: 17px;
								>span:first-of-type{font-size: 22px;}

								>button{
									width: 26px;
									height: 26px;
								}
							}
						}

						>.order-now{
							>button{
								width: 190px;
								padding: 15px;
								font-size: 17px;
							}
						}
					}
				}
			}
		}
	}

	/* @media screen and (min-width: 1400px){
		.menu-wrapper{
			>.content-menu{
				>.pizza{
					>div{
						&:not(:last-of-type){margin-bottom: 0;}
						>.pizza-set{
							display: flex;
							justify-content: space-evenly;
						}
					}
				}
			}
		}
	} */

	@media (min-width: 1440px) {
		.menu-wrapper {
			max-width: 1440px;
			margin: 0 auto 50px;
		}
	}
</style>
