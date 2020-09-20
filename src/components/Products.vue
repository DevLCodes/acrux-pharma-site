<template>
    <div class="products-page">
        <div class="products-header">
            Our Products
        </div>
        <div class="category-filter">
            <ul class="categories">
                <li class="category-item">
                    Diabetic
                </li> 
                <li class="category-item">
                    Paediatric
                </li> 
                <li class="category-item">
                    Gynec
                </li> 
                <li class="category-item">
                    Ortho
                </li> 
                <li class="category-item">
                    Respiratory
                </li> 
                <li class="category-item">
                    Gastro
                </li>  
                <li class="category-item">
                    Urology
                </li>  
                <li class="category-item">
                    General
                </li>  
                <li class="category-item">
                    Cardiac
                </li>    
                <li class="category-item">
                    Antibiotic
                </li>  
                <li class="category-item">
                    Neuro
                </li>    
            </ul>
        </div>
        <div class="products-grid-view">
             <ul class="cards">
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><img src="https://picsum.photos/500/300/?image=10"></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        <p class="card_text">Demo of pixel perfect pure CSS simple responsive card grid layout</p>
                        <button class="btn card_btn">Read More</button>
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><img src="https://picsum.photos/500/300/?image=5"></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        <p class="card_text">Demo of pixel perfect pure CSS simple responsive card grid layout</p>
                        <button class="btn card_btn">Read More</button>
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><img src="https://picsum.photos/500/300/?image=11"></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        <p class="card_text">Demo of pixel perfect pure CSS simple responsive card grid layout</p>
                        <button class="btn card_btn">Read More</button>
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><img src="https://picsum.photos/500/300/?image=14"></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        <p class="card_text">Demo of pixel perfect pure CSS simple responsive card grid layout</p>
                        <button class="btn card_btn">Read More</button>
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><img src="https://picsum.photos/500/300/?image=17"></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        <p class="card_text">Demo of pixel perfect pure CSS simple responsive card grid layout</p>
                        <button class="btn card_btn">Read More</button>
                        </div>
                    </div>
                    </li>
                    <li class="cards_item">
                    <div class="card">
                        <div class="card_image"><img src="https://picsum.photos/500/300/?image=2"></div>
                        <div class="card_content">
                        <h2 class="card_title">Card Grid Layout</h2>
                        <p class="card_text">Demo of pixel perfect pure CSS simple responsive card grid layout</p>
                        <button class="btn card_btn">Read More</button>
                        </div>
                    </div>
                    </li>
                </ul>
        </div>       
     </div>       
</template>

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
             max-width: 1200px;
             margin: 0 auto;
                 h1 {
                    font-size: 24px;
                    font-weight: 400;
                    text-align: center;
                }

                img {
                height: auto;
                max-width: 100%;
                vertical-align: middle;
                }

                .btn {
                color: #ffffff;
                padding: 0.8rem;
                font-size: 14px;
                text-transform: uppercase;
                border-radius: 4px;
                font-weight: 400;
                display: block;
                width: 100%;
                cursor: pointer;
                border: 1px solid rgba(255, 255, 255, 0.2);
                background: transparent;
                }

                .btn:hover {
                background-color: rgba(255, 255, 255, 0.12);
                }

                .cards {
                display: flex;
                flex-wrap: wrap;
                list-style: none;
                margin: 0;
                padding: 0;
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
                background: linear-gradient(to bottom left, #EF8D9C 40%, #FFC39E 100%);
                }

                .card_title {
                color: #ffffff;
                font-size: 1.1rem;
                font-weight: 700;
                letter-spacing: 1px;
                text-transform: capitalize;
                margin: 0px;
                }

                .card_text {
                color: #ffffff;
                font-size: 0.875rem;
                line-height: 1.5;
                margin-bottom: 1.25rem;    
                font-weight: 400;
            }
        }
    }
</style>