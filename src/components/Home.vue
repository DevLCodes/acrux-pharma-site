<template>
  <div class="home" id="home">
    <div class="home-banner" >
      <div class="banner-components">
        <p>Explore our products</p>
         </div>
    </div>
  </div>
</template>

<script>
import image from "../assets/home-banner-flat.png";

export default {
  data: function () {
    return {
      image: image
    };
  },
};
</script>

<style lang="scss">
.home-banner {
  background-image: url(https://source.unsplash.com/_jbClosDsD4/1200x800) ;
  clip: rect(60%,0px,0px,0px);
  background-position: center center;
			background-repeat:  no-repeat;
			background-attachment: fixed;
			background-size:  cover;
			background-color: #999;
  .image {
        height: 150px;
        background-repeat: no-repeat;
    }
  .banner-components {
    width: 100%;
    display: flex;
    flex-flow: row wrap;
    justify-content: flex-start;

    p {
      max-width: 380px;
      font-family: Sacramento;
      font-size: 6.35em;
      color: #272838;
      margin: 5% 12%;
    }
    img {
      max-width: 350px;
      height: auto;
      margin-left: 5rem;
    }
  }
}
@media only screen and (max-width: 920px) {
  .home-banner {
    .banner-components {
      p {
        font-size: 3.25em;
        max-width: 250px;
      }
      img {
        max-width: 300px;
      }
    }
  }
  
}
@media only screen and (max-width: 660px) {
  .home-banner {
    .banner-components {
      width: 100%;
      margin: none;
      p {
        font-size: 2.75em;
      }
      img {
        max-width: 200px;
        height: auto;
      }
    }
  }
}
  @media only screen and (max-width: 540px) {
    .home-banner {
      padding: 2rem 0.5rem;
      .banner-components {
        img {
          margin: 0;
        }
      }
    }
  }
</style>