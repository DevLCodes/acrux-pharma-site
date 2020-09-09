<template>
  <div class="welcome-component">
    <div class="components">
      <img :src="image"/>
      <div class="welcome-content">
        <h1>Welcome to Acrux Pharmaceuticals</h1>
        <p>We are having capacity for large scale productions of tablets, capsules, dry syrups, syrups, nutraceuticals and injections. The motto is ‘for healthy lives’. It is committed to provide quality branded medicines at affordable prices to patients worldwide aiming to reduce health care cost.</p>  
    </div>
    </div>
 </div>
</template>

<script>
    import image from "../assets/welcome-image.png"
    
    export default {
        data: function () {
            return {
                image: image
            }
        }
    }
</script>


<style lang="scss">
  $corange: #EB760A;
  $cgrey : #3E3A37;
  $cblueblack : #272838;
  $ccream : #FAFBFC;
  $cgrey_green: #435466;
  $clightgrey : #DAD9D7;

  .welcome-component{
    height: 610px;
    background-color:$ccream;
    width: 100%;
    .components{
       display: inline-flex;
       margin: 0 10%;
      img{
        max-width: 42%;
        margin: 15px;
      }
      .welcome-content{
           margin-top: 9%;
           padding-left: 5%;
           padding-right: 2%;
        h1{
        font-family: Puritan;
        font-style: normal;
        font-weight: bold;
        font-size: 36px;
        line-height: 40px;
        margin: 8% 0%;
      }
      p{
        font-family: Raleway;
        font-style: normal;
        font-weight: normal;
        font-size: 17px;
        line-height: 39px;
        text-align: justify;
        color: #000000;
      }
      }
      
    }
  }
  @media only screen and (max-width: 600px) {
    .welcome-component{
      height: 528px;
      .components{
       display: inline-flex;
       margin: 0 5%;
      img{
        display:none;
      }
      .welcome-content{
        margin: 5% 5%;
        h1{
            font-family: Puritan;
            font-style: normal;
            font-weight: bold;
            font-size: 36px;
            line-height: 40px;
            margin: 11% 0%;
        }

      }
    }
  }
  }

</style>