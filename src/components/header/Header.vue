<template>
	<header>
		<div class="wrap">
			<img :src="image"/>
			<nav id="menu">
				<li  ><a href="#home">Home</a></li>
				<li ><a href="#product-component">Products</a></li>
				<li ><a href="#career-component">Careers</a></li>
				<li ><a href="#contact-component">Contact</a></li>
			</nav>
			
		</div>
	</header>
</template>

<script>
	import image from "../../assets/logo-text.png"
	import $ from 'jquery'
	export default {
        data: function () {
            return {
                image: image
            }
        },
        methods: {
            display_menu (){
				var body = document.getElementsByTagName("body")[0];
				(!body.classList.contains("display_menu")) ? body.classList.add("display_menu") : body.classList.remove("display_menu");
			}		
        }
    }
	//import vueSmoothScroll from 'vue2-smooth-scroll'
	//Vue.use(vueSmoothScroll)
	/*window.addEventListener("resize", function() {
		close_all_menu();
		document.getElementsByTagName("body")[0].classList.remove("display_menu");
	});*/
	var last_scroll = 0;

	window.onscroll = function() {
		if(!document.getElementById("loader")){
			close_all_menu();
			var header = document.getElementsByTagName("header")[0];
			if(Math.abs(last_scroll - this.scrollY) <= 5) return;
			(this.scrollY < last_scroll) ? header.style.top = "0" : header.style.top = "-" + header.clientHeight + "px" ;
			last_scroll = this.scrollY;
		}
	}

	function close_all_menu() {
		var lis = document.getElementById("menu").getElementsByTagName("li");
		Array.from(lis).forEach(function(e){
			e.style.marginTop = 0;
		});
		var drop_menus = document.getElementsByClassName("drop_menu");
		Array.from(drop_menus).forEach(function(e){
			e.classList.remove("display");
		});
	}


$( () => {
	
	//On Scroll Functionality
	$(window).scroll( () => {
		var windowTop = $(window).scrollTop();
		windowTop > 100 ? $('nav').addClass('navShadow') : $('nav').removeClass('navShadow');
		windowTop > 100 ? $('ul').css('top','100px') : $('ul').css('top','160px');
	});
	
	//Click Logo To Scroll To Top
	$('#logo').on('click', () => {
		$('html,body').animate({
			scrollTop: 0
		},500);
	});
	
	//Smooth Scrolling Using Navigation Menu
	$('a[href*="#"]').on('click', function(e){
		$('html,body').animate({
			scrollTop: $($(this).attr('href')).offset().top - 10
		},500);
		e.preventDefault();
	});
	
	//Toggle Menu
	$('#menu-toggle').on('click', () => {
		$('#menu-toggle').toggleClass('closeMenu');
		$('ul').toggleClass('showMenu');
		
		$('li').on('click', () => {
			$('ul').removeClass('showMenu');
			$('#menu-toggle').removeClass('closeMenu');
		});
	});
	
});
</script>
<style lang='scss'>
	$cblue : #41B883;
	$corange: #EB760A;
	$cgrey : #3E3A37;
	$cblueblack : #272838;
	$ccream : #FAFBFC;
	$cgrey_green: #435466;
	$clightgrey : #DAD9D7;

	$body_height_8: calc((100vh - 113px)/8);
	$body_height_4: calc((100vh - 113px)/4);

i {
	vertical-align: middle;
	display: inline-block;
	background-repeat: no-repeat;
}

html, body {margin: 0;width: 100%;height: 100%; font-size: 14px; font-family: 'Roboto', sans-serif;}
* {box-sizing: border-box;}
body {
	padding-top: 64px;
	overflow-x: hidden;

	&.display_menu{
		overflow-y: hidden;
	}
}
ul {padding: 0; margin: 0;}
li {list-style: none;}
//.wrap {max-width: 1024px; min-width: 320px;}
header {
	display: flex;
	z-index: 1010;
	padding: 10px 0;
	background-color: $cblueblack;
	position: fixed;
	width: 100%;
	max-height: 75px;
	top: 0;
	justify-content: center;
	box-shadow: 0 0 10px 0 rgba(0, 0, 0, .1);
	transition: 0.33s;
}
header .wrap {
	padding: 0 2%;
	width: 94%;
	display: flex;
	align-items: flex-end;
	justify-content: space-between;
}
header img {
	max-width: 140px;
}
header #menu {
	display: flex;
	flex-direction: row;
    margin: 4px 1%;
}
header #menu li {
	position: relative;
	user-select: none;
    min-width: 75px;
    padding: 1% 5%;
	i {width: 12px; height: 12px; background-color: $corange;}
	a {
		color: #EB760A;
		cursor: pointer;
		font-size: 1.35em;
		border: none;
		//border-bottom: 2px solid $corange;
		transition: 0.15s;
		background: none;
		text-decoration: none;
		&:hover {
			border-bottom-color: $corange;
			color: $corange;
			i {
			background-color: $corange;
			}
		}
	}
}




@media screen and (max-width: 660px) {
	body {padding-top: 113px;}
	header {
		max-height: 100px;
	}
	header .wrap {
		justify-content: center;
		align-items: center;
		flex-direction: column;
		padding: 0;
	}
	header img {  
		width: 37%;
		min-height: 49px;

	}
	header #menu{	
			margin: 1px 2%;
			max-width: 95%;
			li{
				min-width: 35px;
				padding: 2% 3%;
				a{
				font-size: 1.15em;
				}
			}
			
	}

}

</style>