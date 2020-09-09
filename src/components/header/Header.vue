<template>
	<header>
		<div class="wrap">
			<img :src="image"/>
			<nav id="menu">
				<li><a>Home</a></li>
				<li><a>Our Products</a></li>
				<li><a>Careers</a></li>
				<li><a>Contact Us</a></li>
			</nav>
			<div id="hamburger" v-on:click="display_menu()">
				<span></span>
				<span></span>
				<span></span>
			</div>
		</div>
	</header>
</template>

<script>
    import image from "../../assets/logo.png"
	window.addEventListener("resize", function() {
		close_all_menu();
		document.getElementsByTagName("body")[0].classList.remove("display_menu");
	});
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
export default {
        name: "ListItemsSfc",
        props: ['items'],
        data() {
            return {
                selectedItem: null,
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
	// eslint-disable-next-line no-unused-vars
/*	var myComp = Vue.extend({
	el: '#app',
	methods: {
			display_menu : function(){
				var body = document.getElementsByTagName("body")[0];
				(!body.classList.contains("display_menu")) ? body.classList.add("display_menu") : body.classList.remove("display_menu");
			}
		}
	});*/
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
body {background-color: #FCA311;padding-top: 113px; overflow-x: hidden; &.display_menu{overflow-y: hidden;}}
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
	width: 100px;
}
header #menu {
	display: flex;
	flex-direction: row;
}
header #menu li {
	position: relative;
	user-select: none;
  margin: 35px 25px;
	i {width: 12px; height: 12px; background-color: $corange;}
	a {
		color: $ccream;
		cursor: pointer;
		font-size: 1.35em;
		border: none;
		//border-bottom: 2px solid $corange;
		transition: 0.15s;
		background: none;
		&:hover {
			border-bottom-color: $corange;
			color: $corange;
			i {
			background-color: $corange;
			}
		}
	}
}
header .drop_menu {
	position: absolute;
	display: block;
	top: 149%;
	transform: scaleY(0);
	width: auto;
    transform-origin: top;
    background-color: $cblueblack;
	transition: 0.25s;
	padding-bottom: 10px;
	box-shadow: 0 2px 5px 0 rgba(0, 0, 0, .1);
	a {
		margin-left: 20px;
		display: block;
		transition: 0.45s;
		opacity: 0;
		margin-right: 20px;
		padding: 10px 0 0 0;
	}
}

header .drop_menu.display {
	transform: scaleY(1);
	a {
		opacity: 1;
	}
}
header #hamburger {
	cursor: pointer;
	border-radius: 50%;
	position: absolute;
	right: 3%;
	top: 30px;
	display: none;
	transform: translateY(-50%);
}
header #hamburger span {
	height: 2px;
	margin-top: 5px;
	margin-bottom: 5px;
	background-color: $corange;
	display: block;
	transition: 0.33s;
	&:nth-child(1) {width: 24px;}
	&:nth-child(2) {width: 24px;}
	&:nth-child(3) {width: 24px;}
}
.display_menu header #hamburger {
	span:nth-child(1) {transform: rotate(45deg) translate(2px, 1px); }
	span:nth-child(2) {transform: rotate(-45deg) ;}
	span:nth-child(3) {transform: rotate(45deg) translate(6px, -9px);}
}



@media screen and (max-width: 660px) {
	body {padding-top: 70px;}
	header .wrap {
		justify-content: center;
		align-items: center;
		flex-direction: column;
		padding: 0;
	}
	header img {width: 50px;}
	header #hamburger {
		display: block;
	}
	header #menu {
		width: 100%;
		display: block;
    height: 0;
    transform-origin: 50% 0;
    transition: 0.33s ease;
		flex-direction: column;
	}
	.display_menu header #menu {
    height: calc(100vh - 285px);
		li {
      height: $body_height_8;
			border-bottom: 1px solid $clightgrey;
      transition: 0.25s ease;
			opacity: 1;
			display: block;
			a {
			}
		}
	}
	header #menu li {
		height: 0;
		opacity: 0;
		margin-left: 0;
    transition: 0.25s ease;
		a {
			left: 0;
      line-height: $body_height_8;
			padding-left: 20px;
			border: none;
			height: 100%;
			width: 100%;
			display: block;
			&:hover {
				color: #ffffff;
				background-color: $cblue;
				i {background-color: #ffffff;}
			}
		}
		i {
			position: absolute;
			right: 20px;
			top: 50%;
			transform: translateY(-50%);
			background-color: $cgrey;
		}
	}
	header .drop_menu {
		top: $body_height_8;
		box-shadow: none;
		left: 0;
		padding-bottom: 0;
		width: 100%;
		a {
			width: 100%;
			padding: 0 !important;
			padding-left: 40px !important;
			margin: 0;
			border-bottom: 1px solid $clightgrey !important;
		}
	}
}
@media screen
and(max-width: 660px)
and(max-height: 500px){
	
	.display_menu header  {
		max-height: 100vh;
		overflow-y: scroll;
	}
	.display_menu header #menu {
		li {
      height: $body_height_4;
      }
	}
	header #menu li {
		a {
         line-height: $body_height_4;
      }
    }
    header .drop_menu {
		top: $body_height_4;
	}
}
i {
	vertical-align: middle;
	display: inline-block;
	background-repeat: no-repeat;
}

</style>