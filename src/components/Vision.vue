<template>
  <div class="vision-component">
    <img :src="image"/>
    <div class="text-block top">
        <h2>Our Vision</h2>
        <p>Our vision is to become a significant major Pharmaceutical Company in INDIA by providing good quality & affordable economical medicine for the treatment of all types of life threatening disease.</p>
    </div>
    <div class="text-block bottom">
        <p>We are meticulously making available pharma products , and constantly improving existing product mix, thereby carving out a niche for ourselves in the field of pharma marketing in India. We shall provide total customer satisfaction through excellent quality control with economically priced Pharmaceutical Products</p>
    </div>
    
 </div>
</template>

<script>
    import image from "../assets/vision-background.png"
    
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
    $lightgrey: #E5E5E5;
    .vision-component{
      height: 1000px;
      background-color: $lightgrey ;
        padding-top: 12px;
        img{
            position: absolute;
            max-width: 50%;
                    
        }
        .text-block{
            background-color: white;
                color: black;
                margin: 4% 3%;
                padding: 2%;
                position: relative;
                z-index: 1;
            h2{
                font-family: Puritan;
                font-style: normal;
                font-weight: bold;
                font-size: 36px;
                line-height: 40px;
                margin: 3% 0%;
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
        .top{
            max-width: 30%;
            margin-left: 9%;
            margin-top: 7%;
        }
        .bottom{
           margin: 10% 9%;
        }
    }
    @media only screen and (max-width: 600px) {
        .vision-component{
            img{
                display:none;

            }
            .text-block{
                margin: 5% 5%;
                h2{
                font-family: Puritan;
                font-style: normal;
                font-weight: bold;
                font-size: 36px;
                line-height: 40px;
                margin: 3% 0%;
                }
            p{
                font-family: Raleway;
                font-style: normal;
                font-weight: normal;
                font-size: 17px;
                line-height: 39px;
                text-align: justify;
                color: #000000;
                padding: 1% 10%;
            }
            }
            .top{
                max-width: none;
            }
            .bottom{
                margin:none;
            }
        }
    }
</style>