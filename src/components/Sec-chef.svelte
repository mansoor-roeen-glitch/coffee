<script>

</script>

<section class="ChefSection_Wrapper" id="OurMenu">
    <div class="ChefSection_Grid">
        <div class="ChefSection_HeaderWrapper">
            <div class="ChefSection_Header">
                <h2 class="MainHeading">History</h2>
                <h3 class="SecondaryHeading">Since 1975, we build the brand of our restaurant around the idea of authentic traditional Italian food from the best quality products.</h3>
                <p class="MainParagraph">Our restaurant was established in 1975. Its founder and first chef was Pietro Savastano. Eccentric men with passion for the italian food and italian way of life. His goal was to create a family place with original, traditional food and an informal atmosphere. Years have passed, but we still value the same things and we are proud of it.</p>
            </div>
        </div>
        <div class="ChefSection_ContentWrapper">
            <div class="ChefSection_Content">
                <ul class="MainList">
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Americano  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Black Coffee  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Cappuccino  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Espresso  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Latte  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Macchiato  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                    <li class="MainList_Item">
                        <span class="MainList_Item_left">Cold Coffee Variety  </span>
                        <span class="MainList_Item_Right">15.00 €</span>
                    </li>
                </ul>
                <a class="MainButton" href="/">Learn more</a>
            </div>
        </div>
        <div class="ChefSection_ImageWrapper">
            <div class="ChefSection_Image">
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img class="ChefSection_Img" id="ChefSection_Img" alt="Coffee shop image" src="/images/Chef.png">
            </div>
        </div>
    </div>
</section>

<style>
    
    .ChefSection_Wrapper {
        width: 100%;
        height: fit-content;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .ChefSection_Grid {
        max-width: 1480px;
        padding: 0px 20px;
        position: relative;
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-template-rows: repeat(11, 1fr);
    }

    .ChefSection_Wrapper::before {
        content: "";
        position: absolute;
        top: 0px;
        left: 0px;
        width: calc(50% - 120px);
        height: 480px;
        background: var(--white-c);
        z-index: -1;
    }

    .ChefSection_Wrapper::after {
        content: "";
        position: absolute;
        bottom: 120px;
        left: 0px;
        width: 50%;
        height: 360px;
        background: var(--white-b);
        z-index: -1;
    }

    .ChefSection_HeaderWrapper {
        grid-area: 2 / 6 / 7 / 13;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
    }   

    .ChefSection_Header {
        padding: 120px;
        position: relative;
    }

    .MainHeading {
        color: var(--brown);
        text-transform: uppercase;
        font-family: "Jost", sans-serif;
        font-size: 1rem;
        letter-spacing: 1px;
        padding-bottom: 1.5rem;
    }

    .SecondaryHeading {
        color: var(--black-b);
        font-family: "Playfair Display", serif;
        font-size: 1.3rem;
        line-height: 1.7;
    }

    .MainParagraph {
        margin-top: 30px;
        color: rgb(119, 119, 119);
        font-size: 1.125rem;
        line-height: 1.7;
        font-family: "Jost", sans-serif;
    }

    .ChefSection_ImageWrapper {
        grid-area: 3 / 1 / 9 / 5;
    }

    .ChefSection_Image, .ChefSection_Img {
        width: 100%;
    }

    .ChefSection_ContentWrapper {
        grid-area: 7 / 7 / 15 / 13;
        background: rgb(22, 25, 26);
        position: relative;
        padding: 120px;
    }

    .ChefSection_ContentWrapper::before {
        content: "";
        position: absolute;
        top: 0px;
        left: 0px;
        width: 50vw;
        height: 100%;
        background: rgb(22, 25, 26);
        z-index: -1;
    }
    
    .ChefSection_Content {
        position: relative;
        height: fit-content;
        list-style: none;
    }

    .MainList_Item {
        padding: 0.2rem 0px;
        display: flex;
        -webkit-box-pack: justify;
        justify-content: space-between;
        z-index: 1;
        position: relative;
    }

    .MainList_Item::before {
        content: "";
        border-top: 2px dotted var(--white-c);
        opacity: .6;
        position: absolute;
        left: 0px;
        top: 50%;
        width: 100%;
        height: 100%;
        z-index: -1;
    }

    .MainList_Item_left {
        padding: 0.5rem 1rem 0.5rem 0px;
        background: rgb(22, 25, 26);
        color: var(--white);
        font-family: "Playfair Display", serif;
        font-size: 1.125rem;
        text-transform: uppercase;
    }

    .MainList_Item_Right {
        padding: 0.5rem 0px 0.5rem 1rem;
        background: rgb(22, 25, 26);
        color: var(--white);
        font-size: 1.125rem;
        letter-spacing: 1px;
    }

    .MainButton {
        display: block;
        overflow: hidden;
        margin-top: 2rem;
        padding: 0.625rem 2rem;
        align-self: flex-start;
        font-size: 0.875rem;
        font-weight: 400;
        color: var(--white-b);
        border: 2px solid var(--white-b);
        opacity: .8;
        text-transform: uppercase;
        letter-spacing: 1px;
        cursor: pointer;
        z-index: 1;
        position: relative;
        width: fit-content;
        text-decoration: none;
        font-family: "Jost", sans-serif;
    }

    .MainButton::before {
        content: "";
        position: absolute;
        width: 0px;
        height: 100%;
        top: 0px; 
        left: 0px;
        background: var(--white-b);
        z-index: -1;
    }

    .MainButton:hover::before {
        animation: animBtn .4s ease forwards;
    }

    .MainButton:hover {
        color: var(--black);
    }

    @media screen and (max-width: 1370px) {
        .ChefSection_ContentWrapper {
            grid-area: 6 / 7 / 15 / 12; 
        }

        .ChefSection_HeaderWrapper {
            grid-area: 1 / 6 / 7 / 13;
        }
    }

    @media screen and (max-width: 1210px) {
        .ChefSection_Grid {
            width: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            
        }

        .ChefSection_Header {
            padding: 80px;
            width: 100%;
        }

        .ChefSection_ContentWrapper {
            width: 88%;
            padding: 80px;
        }

        .ChefSection_Image {
            padding-top: 80px;
            width: 100%;
            height: fit-content;
            justify-content: center;
            align-items: center;
        }

        .ChefSection_Img {
            width: 500px;
            height: 720px;
        }

    }

    @media screen and (max-width: 600px) {
        .ChefSection_Wrapper::after {
            content: "";
            position: absolute;
            bottom: 300px;
            left: 0px;
            width: 100vw;
            height: 580px;
            background: var(--white-b);
            z-index: -1;
        }

        .ChefSection_Img {
            width: 100%;
            height: auto;
        }

        .ChefSection_ImageWrapper {
            padding-top: 0px;
            width: 90%;
        }

        .ChefSection_Grid {
            padding: 0px!important;
        }

        .ChefSection_Header {
            width: 94%;
        }
    }

    @media screen and (max-width: 1000px) {
        .ChefSection_Header {
            padding: 80px 0px;
            width: 85%;
        }
    }

</style>