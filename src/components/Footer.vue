<template>
	<footer class="footer-container">
		<div class="footer-nav">
			<div class="logo"><p>pizzashop</p></div>
			
			<div class="nav">
				<p>Home</p>
				<ul>
					<li>To Order</li>
					<li>About us</li>
					<li>Events</li>
					<li>Menu</li>
				</ul>
			</div>
			
			<div class="nav">
				<p>Events</p>
				<ul>
					<li>3 Pizza 1 Free Coffee</li>
					<li>2 Pizza for 1 Price</li>
					<li>Kitchen Tour</li>
				</ul>
			</div>
			
			<div class="nav">
				<p>Menu</p>
				<ul>
					<li>Show All</li>
					<li>Seaproducts</li>
					<li>Vegan</li>
					<li>Meat</li>
				</ul>
			</div>
			
			<div class="nav">
				<p>About us</p>
				<ul>
					<li>Our History</li>
					<li>Why We?</li>
				</ul>
			</div>
		</div>

		<div class="footer-contacts">
			<div class="number">
				<a href="tel:+7 (937) 333-55-33">+7 (937) 333-55-33</a>
			</div>

			<div class="social">
				<a href="#"><img src="../assets/img/instagram.png" alt="instagram"></a>
				<a href="#"><img src="../assets/img/twitter.png" alt="twitter"></a>
				<a href="#"><img src="../assets/img/facebook.png" alt="facebook"></a>
			</div>
		</div>
	</footer>
</template>

<script>

</script>

<style scoped lang="scss">
	.footer-container{
		padding: 0 5% 40px;
		display: flex;
		flex-direction: column;
		
		>.footer-nav {
			margin-bottom: 40px;
			display: flex;
			flex-wrap: wrap;
			
			>.logo{
				width: 100%;
				font-style: normal;
				font-weight: 800;
				font-size: 23.7564px;
				line-height: 109.5%;
				background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
				-webkit-background-clip: text;
				-webkit-text-fill-color: transparent;
				background-clip: text;
				margin-bottom: 40px;
			}

			>.nav{
				width: 100%;
				margin-bottom: 30px;

				>p:first-child{
					font-style: normal;
					font-weight: 400;
					font-size: 15.3469px;
					line-height: 125.68%;
					letter-spacing: -0.02em;
					color: #A3A3A3;
					margin-bottom: 15px;
				}

				>ul{
					li{
						cursor: pointer;
						font-style: normal;
						font-weight: 400;
						font-size: 13.8604px;
						line-height: 125.68%;
						letter-spacing: -0.02em;
						color: #515151;

						&:not(:last-of-type){margin-bottom: 10px;}

						&:hover{
							background: linear-gradient(261.69deg, #FF6432 12.12%, #FFA228 86.72%);
							-webkit-background-clip: text;
							-webkit-text-fill-color: transparent;
							background-clip: text;
						}
					}
				}
			}
		}

		>.footer-contacts{
			display: flex;
			align-items: center;
			justify-content: space-between;

			>.number{
				font-style: normal;
				font-weight: 400;
				font-size: 14.4561px;
				line-height: 125.68%;
				letter-spacing: -0.02em;
				background: linear-gradient(261.69deg, #FF612E 12.12%, #FFA32B 86.72%);
				-webkit-background-clip: text;
				-webkit-text-fill-color: transparent;
				background-clip: text;
				opacity: 1;

				&:hover{opacity: 0.7;}
			}

			>.social{
				display: flex;
				align-items: center;
				
				a{
					position: relative;
					height: 30px;
					width: 30px;
					background: linear-gradient(261.69deg, #FF612E 12.12%, #FFA32B 86.72%);
					border-radius: 50%;
					opacity: 1;
					
					&:not(:last-of-type){margin-right: 15px;}
					>img{position: absolute;}

					&:first-of-type{
						>img{
							top: 4.5px;
							left: 5px;
						}
					}

					&:nth-child(2){
						>img{
							top: 3px;
							left: 3px;
						}
					}

					&:last-of-type{
						>img{
							top: 4px;
							left: 5px;
						}
					}

					&:hover{opacity: 0.7;}
				}
			}
		}
	}

	@media screen and (min-width: 360px){
		.footer-container{
			>.footer-nav {
				>.nav{width: 50%;}
			}
		}
	}

	@media screen and (min-width: 600px	){
		.footer-container{
			>.footer-nav {
				display: flex;
				flex-wrap: wrap;
				justify-content: space-between;

				>.nav{width: inherit;}
			}
		}
	}

	@media screen and (min-width: 1000px){
		.footer-container{
			padding-top: 70px;
			>.footer-nav {
				>.logo{
					font-size: 29.8532px;
					width: inherit;
					margin-bottom: 0;
				}

				>.nav{
					>p:first-child{font-size: 19.6259px;}
					>ul{
						li{font-size: 17.7249px;}
					}
				}
			}

			>.footer-contacts{
				>.number{font-size: 20.881px;}

				>.social{
					>a{
						width: 40px;
						height: 40px;

						>img{
							width: 30px;
							height: 30px;
						}

						&:first-of-type{
							>img{
								top: 4.5px;
								left: 5.5px;
							}
						}

						&:nth-child(2){
							>img{
								top: 6px;
								left: 5px;
							}
						}

						&:last-of-type{
							>img{
								top: 5px;
								left: 5px;
							}
						}
					}
				}
			}
		}
	}

	@media (min-width: 1440px) {
		.footer-container {
			max-width: 1440px;
			margin: 0 auto;
		}
	}
</style>