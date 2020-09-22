<template>
  <div class="home" id="home">
    <div class="home-banner">
      <div class="banner-components">
        <p>Explore our products</p>
        <img :src="image" />
      </div>
    </div>
  </div>
</template>

<script>
import image from "../assets/home-banner-flat.png";

export default {
  data: function () {
    return {
      image: image,
    };
  },
};
</script>

<style lang="scss">
.home-banner {
  background-color: #fca311;
  .banner-components {
    width: 100%;
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    justify-content: center;
    p {
      max-width: 380px;
      font-family: Sacramento;
      font-size: 6.35em;
      color: #272838;
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
      width: 98%;
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
          display: none;
        }
      }
    }
  }
</style>