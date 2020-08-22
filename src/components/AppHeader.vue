<!-- Main Template For Header -->
<template>
	<div>
		<!-- Header Of the Site -->
		<div class="header">
			<!-- Overlay -->
			<div class="overlay"></div>
			<!-- Nav Bar -->
			<div class="nav-bar">
				<div class="container">
					<div class="row">
						 
						 <div class="col">
						 	<div class="mobile-logo">
						 		<img src="../assets/logo-mobile.png" alt="Mobile Logo">
						 	</div>
						 </div>

						 <div class="col">
						 	<div class="toggle-bar">
						 		<i v-on:click="showSide()" class="fas fa-bars"></i>
						 	</div>
						 </div>

					</div>
				</div>
			</div>
			<!-- Left Side -->
			<div class="left-header-side">
				<!-- Logo -->
				<div class="logo">
					<a href="#"><img src="../assets/logo.png" alt="Logo Image"></a>
				</div>
				<!-- Main List -->
				<div class="main-list">
					<ul class="list-unstyled">
						<li><a class="active" href="#">Home</a></li>
						<li><a href="#">Services</a></li>
						<li><a href="#">Our Work</a></li>
						<li><a href="#">About Us</a></li>
						<li><a href="#">Recent News</a></li>
						<li><a href="#">Testimonials</a></li>
						<li><a href="#">Contact</a></li>
					</ul>
				</div>
			</div>
			<!-- Replaced Left Side Bar -->
			<div class="replaced-left-side-bar" v-bind:class="{show: show}">
				<!-- Closed Item -->
				<div class="close">
					<i v-on:click="showSide()" class="far fa-window-close"></i>
				</div>
				<!-- Replaced Main List Items -->
				<div class="main-list">
					<ul class="list-unstyled">
						<li><a class="active" href="#">Home</a></li>
						<li><a href="#">Services</a></li>
						<li><a href="#">Our Work</a></li>
						<li><a href="#">About Us</a></li>
						<li><a href="#">Recent News</a></li>
						<li><a href="#">Testimonials</a></li>
						<li><a href="#">Contact</a></li>
					</ul>
				</div>
			</div>
			<!-- Right Side -->
			<div class="right-header-side">
				<div class="right-header-side-content">
					<h1>One Page <span>Pro</span></h1>
					<h2>One <br /> Page <br /> <span>Pro</span></h2>
					<h3>Provide all-in-one-service .</h3>
					<button class="text-uppercase btn">explore more<i class="fas fa-long-arrow-alt-right"></i></button>
				</div>
			</div>
		</div>
	</div>
</template>

<!-- Main Script For Header -->
<script>


	export default{
		name: 'app-header',
		data() {
			return {
				show: false
			}
		},

		methods: {
			showSide() {
				this.show = !this.show;
			}
		}
	};
</script>

<!-- Main Style For Header -->
<style scoped>

/*******************************************/
/************* Start Header ****************/
	.header{
		height: 100vh;
		width: 100%;
		background: url("../assets/header/bg-main.jpeg");
		background-size: cover;
		-webkit-background-size: cover;
		-moz-background-size: cover;
		-o-background-size: cover;
		-ms-background-size: cover;
		background-position: center;
		position: relative;
	}

	.header .overlay{
		position: absolute;
		top: 0; bottom: 0;
		left: 0; right: 0;
		background-color: rgba(0,0,0,.3);
		z-index: 1;
	}

	.header .left-header-side{
		position: fixed;
		top: 0;
		bottom: 0;
		left: 0;
		width: 23%;
		background-color: rgba(0,0,0,.7);
		z-index: 2;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding-top: 5%;
	}

	.header .left-header-side .logo img{
		width: 190px;
		margin-bottom: 2.5rem;
	}

	.header .left-header-side .main-list ul{
		margin-bottom: 0;
	}

	.header .left-header-side .main-list ul li{
		text-align: center;
    	padding: 15px 0
	}

	.header .left-header-side .main-list ul li a{
		text-decoration: none;
	    color: var(--gray-color);
	    font-weight: 600;
	    text-transform: uppercase;
	    font-size: 17px;
	    transition: color .4s ease-in-out;
	}

	.header .left-header-side .main-list ul li a.active,
	.header .left-header-side .main-list ul li a:hover{
		color: #fff;
	}

	.header .right-header-side{
		position: absolute;
		z-index: 2;
		top: 0;
		right: 0;
		bottom: 0;
		width: 77%;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.header .right-header-side .right-header-side-content{
		position: relative;
		left: 12%;
	}

	.header .right-header-side .right-header-side-content h1{
		color: #fff;
	    font-size: 8rem;
	    font-weight: 700;
	    text-transform: uppercase
	}

	.header .right-header-side .right-header-side-content h2{
		display: none;
	}

	.header .right-header-side .right-header-side-content h1 span{
		color: var(--main-color);
	}

	.header .right-header-side .right-header-side-content h3{
		color: var(--main-color);
	    font-size: 3.5rem;
	    font-weight: 400;
        margin-bottom: 6rem
	}

	.header .right-header-side .right-header-side-content button{
	    color: #fff;
	    font-weight: 500;
	    letter-spacing: .1rem;
	    padding: .8rem 0;
	    border-bottom: 1px solid var(--main-color);
	}

	.header .right-header-side .right-header-side-content button i{
		position: relative;
		left: 2%;
		transition: left .3s ease-in-out;
	}

	.header .right-header-side .right-header-side-content button:hover  i{
		left: 6%;
	}

	/* Start Mobile Style */
	.nav-bar{
		background-color: #000;
		padding: 1.1rem 0;
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		z-index: 1000;
		display: none;
	}

	.header .toggle-bar{
		text-align: right;
	}

	.header .toggle-bar i{
		color: #fff;
		font-size: 2rem;
		cursor: pointer;
	}

	.header .replaced-left-side-bar{
		position: fixed;
		top: 0;
		bottom: 0;
		right: 0;
		width: 400px;
		background-color: rgba(0,0,0,.8);
		z-index: 999;
		display: flex;
		flex-direction: column;
		padding: 8rem 0;
		transform: translateX(100%);
		transition: transform 1.5s ease-in-out;
	}

	.header .replaced-left-side-bar .close{
		padding-left: 10%;
	}

	.header .replaced-left-side-bar .close i{
		color: #fff;
		cursor: pointer;
	}

	.header .replaced-left-side-bar.show{
		transform: translateX(0);
	}

	.header .replaced-left-side-bar ul{
		margin-bottom: 0;
	    width: 80%;
	    margin: 0 auto
	}

	.header .replaced-left-side-bar ul li{
		padding: 1rem .2rem;
    	border-bottom: 1px solid var(--gray-color);
	}

	.header .replaced-left-side-bar ul li a{
	    text-decoration: none;
	    color: var(--gray-color);
	    font-weight: 500;
	    text-transform: uppercase;
	    transition: color .3s ease-in-out;
	}

	.header .replaced-left-side-bar ul li a:hover{
		color: #fff;
	}

	/* End Mobile Style */

	/* Start Media Query For Mobile and Tablet */

	@media screen and (max-width: 992px) {
		.nav-bar{
			display: block;
		}

		.header .left-header-side{
			display: none;
		}

		.header .right-header-side{
			width: 100%;
		}
		.header .right-header-side .right-header-side-content{

		}

		.header .right-header-side .right-header-side-content h1{
			font-size: 5rem;
		}

		.header .right-header-side .right-header-side-content h3{
		    font-size: 2rem;
   			margin-bottom: 3rem	
		}

		.header .right-header-side .right-header-side-content button{
			font-size: 14px
		}
	}

	@media screen and (max-width: 768px) {
		.header .right-header-side .right-header-side-content h1{
	    	font-size: 4rem
		}

		.header .right-header-side .right-header-side-content h3{
		    font-size: 1.5rem;
		    margin-bottom: 1.5rem	
		}

		.header .right-header-side .right-header-side-content button{
			
		}	
	}

	@media screen and (max-width: 575px) {
		.header .right-header-side .right-header-side-content{
			text-align: center;
			left: 0;
		}
		.header .right-header-side .right-header-side-content h1{
	    	display: none;
		}

		.header .right-header-side .right-header-side-content h2{
	    	display: block;
	    	color: #fff;
		    font-weight: 700;
		    text-transform: uppercase;
		    font-size: 4rem;
		}

		.header .right-header-side .right-header-side-content h2 span{
	    	color: var(--main-color);
		}
	}

	/* End Media Query For Mobile and Tablet */

/*******************************************/
/************* End Header ****************/

</style>






