<template>
    <div class="products-page" id="product-component">
        <div class="products-header">
            Our Products
        </div>
        
        <div class="products-grid-view">
             <ul class="cards">
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"> <span class="helper"></span><img :src="calrace60k"/></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"> <span class="helper"></span><img :src="calrace"/></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"> <span class="helper"></span><img :src="cefmont200"/></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><span class="helper"></span><img :src="dezafort"/></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><span class="helper"></span><img :src="calrace60k"/></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><span class="helper"></span><img :src="calrace60k"/></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        </div>
                    </div>
                    </li>
                </ul>
        </div>       
     </div>       
</template>
<script>
    import calrace60k from "../../src/assets/calrace60k.jpg"
    import calrace from "../../src/assets/Calrace.jpg"
    import cefmont200 from "../../src/assets/Cefmont200.jpg"
    import dezafort from "../../src/assets/DezaFort.jpg"
    import enzamact from "../../src/assets/Enzamact.jpg"
    import icobalp from "../../src/assets/Icobal-P.jpg"
	export default {
        data: function () {
            return {
                calrace60k: calrace60k,
                calrace: calrace,
                cefmont200: cefmont200,
                dezafort: dezafort,
                enzamact: enzamact,
                icobalp:icobalp

            }
        }
    }
</script>
<style lang="scss">
    .products-page{
        background: white;
        min-height: 1000px;
        .products-header{
            padding: 2% 2%;
            font-size: 53px;
        }
        .category-filter{
             display: inline-flex;
             min-width: 85%;
             .categories{
                display: flex;
                flex-wrap: wrap;
                list-style: none;
                margin: 0;
                padding: 0;
                .category-item{
                    margin: 1% 4%;
                    min-width: 100px;
                    padding: 1rem;
                    background-color: #ffd9a0;
                    border-radius: 2.25rem;
                    box-shadow: 0 20px 40px -14px rgba(0, 0, 0, 0.25);
                    display: flex;
                    flex-direction: column;
                    overflow: hidden;
                }
             }
             
        }
        .products-grid-view{
             max-width: 1400px;
             margin: 0 auto;
                 h1 {
                    font-size: 24px;
                    font-weight: 400;
                    text-align: center;
                }

                img {
               
                max-height: 100%;
                max-width: 100%;
                vertical-align: middle;
                }

                .helper {
                    display: inline-block;
                    height: 100%;
                    vertical-align: middle;
                }

                .cards {
                display: flex;
                flex-wrap: wrap;
                list-style: none;
                margin: 0;
                padding: 0;
                }
                .card_image{
                   height: 325px;
                   width: 450px;
                   text-align: center;
                }

                .cards_item {
                display: flex;
                padding: 1rem;
                }

                @media (min-width: 40rem) {
                .cards_item {
                    width: 50%;
                }
                }

                @media (min-width: 56rem) {
                .cards_item {
                    width: 33.3333%;
                }
                }

                .card {
                background-color: white;
                border-radius: 0.25rem;
                box-shadow: 0 20px 40px -14px rgba(0, 0, 0, 0.25);
                display: flex;
                flex-direction: column;
                overflow: hidden;
                }

                .card_content {
                padding: 1rem;
                background: linear-gradient(to bottom left, #272838 40%, #030506b8 100%);
                }

                .card_title {
                color: #ffffff;
                font-size: 1.1rem;
                font-weight: 700;
                letter-spacing: 1px;
                text-transform: capitalize;
                margin: 0px;
                }

        }
    }
</style>