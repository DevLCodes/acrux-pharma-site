<template>
    <footer class="footer-distributed">
		<div class="row-1">
			<div class="footer-left">
				<div class="icon-card">
					<img :src="image"/>
					<ul>
						<li> <i class="fas fa-phone-alt"></i> <a>9943887414</a> </li>
						<li> <i class="far fa-envelope"></i>  <a>acruxpharmaceuticals@gmail.com</a> </li>   
						<li> <i class="far fa-address-card"></i> <a>116/9, Hussaina Complex, Palakkarai, Trichy-620008</a> </li>   
					</ul>
				</div>
			</div>
			<div class="footer-right">  
					<div class='content'>Follow us</div>
					<div class='icons'>
						<a> <i class="fab fa-twitter"></i> </a>
						<a> <i class="fab fa-facebook-f"></i> </a>
						<a> <i class="fab fa-linkedin"></i> </a>
						<a> <i class="fab fa-instagram"></i> </a>
					</div>
			</div>
		</div>
		<div class="row-2">
			<div class='copyright_area'>
				<p> Copyright &copy; 2020. Powered by <a>Lokesh Kumar</a></p>
			</div>  
		</div>
	</footer>
</template>
<script>
    import image from "../../assets/logo-text.png"
    
    export default {
        data: function () {
            return {
                image: image
            }
        }
    }
</script>


<style lang="scss">
$p-font-sizes: (
  null  : 8px,
  480px : 10px,
  640px : 14px,
  1024px: 20px
);
@mixin font-size($fs-map) {
  @each $fs-breakpoint, $fs-font-size in $fs-map {
    @if $fs-breakpoint == null {
      font-size: $fs-font-size;
    }
    @else {
      @media screen and (min-width: $fs-breakpoint) {
        font-size: $fs-font-size;
      }
    }
  }
}
footer{
	bottom: 0;
	width: 100%;
	.row-1{
		width: inherit;
		display: inline-flex;
		background-color: #172131;
		box-sizing: border-box;
		text-align: left;
		padding: 15px 8%;
		vertical-align: top;
		.footer-left{
			width: 40%;
			.icon-card{
				display:inline-flex;
				padding:20px;
				img{
					max-width: 200px;
					padding: 5% 3%;
					margin-right: 8px;
				}
				ul {
					margin: 0;
					list-style-type: none;
				}

				li {
				margin: 0;
				color: #d0c9c9;
				font-size: 13px;
				font-weight: 300;
				line-height: 22px;
				list-style-type: none;
				text-align: left;
				padding: 1.5%;
				min-width: 251px;

				a{
				margin-left: 3%;
				color: #989898;
				}
			}
		}
	}
	.footer-right{
		width: 22%;
		margin: 3px 0 0 20%;
	.content{
        font-size: 20px;
		color: #d4d4d4;
		font-family: Puritan;
		text-align: center;
	}
      .icons{
        margin-top: 7%;
		width: auto;
          a{
            padding: 3.5%;
			margin: 4%;
            font-size: 30px;
            color: #070617;
            background-color: white;
            border-radius: 54%;
            border: 1px solid grey;
               
          }
      }
	}
	
}
.row-2{
      background: #080B15;
      padding: 1px;
     .copyright_area{
      bottom: 0;
    }
   }
}


 


@media screen and (max-width: 660px) {

footer{
	.row-1{
		display: block;
		.footer-left{
			width: 100%;
			margin: 0 9%;
			.icon-card{
				img{
					max-width: 200px;
					padding: 5% 3%;
					margin: 0% 2%;
				}
			}
		}
		.footer-right{
			width: 100%;
			margin: 3% 1%;
			.icons{
				a{
					padding: 3%;
					margin: 4%;
				}
			}
		}
	}
}
	.row-1{
	
	.icon-card{
		ul {
		display: none;
		}

        li {
        margin: 0;
        color: #666666;
        font-size: 13px;
        font-weight: 300;
        line-height: 22px;
        list-style-type: none;
        text-align: left;
        padding: 6px;

        a{
          margin-left:20px;
        }
      }
	}
}
}
</style>