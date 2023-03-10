<template>
	<section class="menu-wrapper" id="menu">
		<div class="title">
			<p>Menu</p>
		</div>

		<div class="content-menu">
			<!---------------------------------------->
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
				
			</div>
			<!---------------------------------------->
			<div class="pizza-img">
				
			</div>
			<!---------------------------------------->
			<div class="pizza">

			</div>
		</div>
	</section>
</template>

<script>
	export default {
		data(){
			return{
				activeTab: 'show',
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
		}
	}

	@media (min-width: 1440px) {
		.menu-wrapper {
			max-width: 1440px;
			margin: 0 auto 50px;
		}
	}
</style>
