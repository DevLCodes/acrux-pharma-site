<template>
  <div class="home">
      <div class="home-banner">
        <div class="banner-components">
            <p> Explore our products</P>
            <img :src="image"/>
        </div>
      </div>
  </div>
</template>

<script>
    import image from "../assets/home-banner-flat.png"
    
    export default {
        data: function () {
            return {
                image: image
            }
        }
    }
</script>

<style lang="scss">
.home-banner{
    height: 385px;
    background-color: #FCA311;
    display: inline-flex;
    width: -webkit-fill-available;
    .banner-components{
        margin: 10px 14%;
        width: 80%;

      p{
    position: absolute;
    width: 20%;
    font-family: Sacramento;
    font-style: normal;
    font-weight: normal;
    font-size: 6.35em;
    line-height: 121px;
    color: #FBF8F8;
    margin: 3% 60px 10px;
    }
      img{
      position: absolute;
      max-width: 350px;
      height: auto;
    }
    }
}
@media only screen and (max-width: 600px) {

.home-banner{

    .banner-components{
       margin: 16px 7%;
       width: 98%;
       display: inline-block;
      p{
        position: absolute;
        width: auto;
        font-family: Sacramento;
        font-style: normal;
        font-weight: normal;
        font-size: 3.75em;
        line-height: 121px;
        color: #FBF8F8;
        margin: initial;
      }
      img{
      position: inherit;
      max-width: 237px;
      height: auto;
      margin: 23% 10px 10px;
    }
    }
}
}
</style>