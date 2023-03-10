<template>
	<section class="menu-wrapper" id="menu">
		<div class="title">
			<p>Menu</p>
		</div>

		<div class="content-menu">
			<!---------------------------------------->
			<div class="choose-btns">
				<div>
					<button>Show All</button>
				</div>
				<div>
					<button>Meat</button>
				</div>
				<div>
					<button>Vegetarian</button>
				</div>
				<div>
					<button>Sea products</button>
				</div>
				<div>
					<button>Mushroom</button>
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

</script>

<style scoped lang="scss">
	@import '../assets/vars';
	@import '../assets/extends';

	.menu-wrapper{
		display: flex;
		flex-direction: column;
		align-items: center;

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

				>div{
					>button{@extend %allButtons;}
				}
			}
		}
	}
</style>