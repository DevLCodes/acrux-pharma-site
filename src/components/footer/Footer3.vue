<template>
  <div id='footer' class='footer'>
     <div class='row-1'>
      <div class="icon-card">
        <img :src="image"/>
        <ul>
            <li> <i class="fas fa-phone-alt"></i> <a>9943887414</a> </li>
            <li> <i class="far fa-envelope"></i>  <a>acruxpharmaceuticals@gmail.com</a> </li>   
            <li> <i class="far fa-address-card"></i> <a>116/9, Hussaina Complex, Palakkarai, Trichy-620008</a> </li>   
        </ul>
      </div>
      <span class='social-banner'>  
        <div class='content'>Follow us</div>
          <div class='icons'>
              <a> <i class="fab fa-twitter"></i> </a>
              <a> <i class="fab fa-facebook-f"></i> </a>
              <a> <i class="fab fa-linkedin"></i> </a>
              <a> <i class="fab fa-instagram"></i> </a>
          <div>
        </div>
      </div>
      </span>
      </div>
    <div class='row-2'>
      <div class='copyright_area'>
        <p> Copyright &copy; 2020. Powered by <a>Lokesh Kumar</a></p>
      </div>  
    </div>
 </div>
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

  .footer{
      width:100%;
      z-index:100;

    .row-1{ 
    position: inherit;
    height: 150px;
    background-color: #070617;
    clear: both;
    bottom: 0;
    left: 0;
    display: inline-flex;
    margin-right: auto;
    margin-left: auto;

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
    .social-banner{
      color: white;
      margin: 19px 10px 10px;

      .content{
       @include font-size($p-font-sizes);
      }

      .icons{
         margin-top: 21px;
          a{
            padding: 9px;
            margin: 17px;
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
      background: #a0a0a0;
      padding: 1px;
     .copyright_area{
      bottom: 0;
    }
   }
  }
</style>