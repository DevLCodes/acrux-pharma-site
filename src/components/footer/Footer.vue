<template>
  <div id='footer' class='footer'>
    <span class='social-banner'>  
      <div class='content'>Follow us on social media</div>
      <div class='icons'>
        <a> <i class="fab fa-twitter"></i> </a>
        <a> <i class="fab fa-facebook-f"></i> </a>
        <a> <i class="fab fa-linkedin"></i> </a>
        <a> <i class="fab fa-instagram"></i> </a>
      <div>
   
  </div>
       </div>
    </span>
  <div class='copyright_area'>
    <p> Copyright © 2020. Powered by <a>Lokesh Kumar</a>
    </p>
    
  </div>  
 </div>
</template>

<script>

</script>


<style lang="scss">

$p-font-sizes: (
  null  : 20px,
  480px : 26px,
  640px : 36px,
  1024px: 46px
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
    width: 100%;
    position: inherit;
    height: 150px;
    background-color: #070617;
    clear: both;
    bottom: 0;
    left: 0;
    display: block;
    
    .social-banner{
      display: inline-flex;
      color: white;
      margin: 19px 10px 10px;

      .content{
       @include font-size($p-font-sizes);
      }

      .icons{
          margin : 14px 5px 5px 175px;
          a{
            padding : 15px;
            font-size: 30px;
          }

      }
    }
    .copyright_area{
      bottom: 0;
    }
  }
</style>