<script>
</script>

<section class="AboutSection_Wrapper" id="About">
    <div class="AboutSection_Grid">
        <div class="AboutSection_HeaderWrapper">
            <div class="AboutSection_Header">
                <h2 class="MainHeading">About us</h2>
                <h3 class="SecondaryHeading">We believe that coffee can bring people together, so we care for every detail, to make your visit here unforgettable.</h3>
            </div>
        </div>
        <div class="AboutSection_ContentWrapper">
            <div class="AboutSection_Content">
                <p class="MainParagraph">We are famous in Sicilia, cause we cook our dishes from the freshest ingredients in traditional way. Local vegetables, fresh fish and own winery. We specialize in homemade classic Italian pizza, pasta, salads, soups and much more. Don't forget to try our Lasagna. We provide excellent taste, great service and warm atmosphere.</p>
                <a class="MainButton" href="/">Learn more</a>
            </div>
        </div>
        <div class="AboutSection_ImageWrapper">
            <div class="AboutSection_Image">
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img class="AboutSection_Img" id="AboutSection_Img" alt="Image of two guys making something" src="/images/About.png">
            </div>
        </div>
    </div>
</section>

<style>
 
    .AboutSection_Wrapper {
        width: 100%;
        height: fit-content;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .AboutSection_Wrapper::after {
        content: "";
        z-index: -2;
        position: absolute;
        top: 50%;
        left: 0px;
        width: 100%;
        height: calc(50% - 120px);
        background: var(--white-b);
    }

    .AboutSection_Grid {
        max-width: 1480px;
        padding: 0px 20px;
        position: relative;
        display: grid;
        grid-template-rows: repeat(8, 1fr);
        grid-template-columns: repeat(12, 1fr);
    }

    .AboutSection_Wrapper::before {
        content: "";
        position: absolute;
        top: -120px;
        left: 50%;
        width: 2px;
        height: 240px;
        background: var(--white-b);
    }

    .AboutSection_HeaderWrapper {
        grid-area: 1 / 1 / 5 / 7;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
        flex-direction: column;
        padding: 120px
    }

    .AboutSection_ContentWrapper {
        background: var(--black-b);
        grid-area: 3 / 7 / 7 / 13;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
        position: relative;
        padding: 120px 0px 120px 120px;
    }

    .AboutSection_ContentWrapper::before {
        content: "";
        position: absolute;
        top: 0px;
        left: 0px;
        width: 50vw;
        height: 100%;
        background: rgb(22, 25, 26);
        z-index: -1;
    }

    .AboutSection_ImageWrapper {
        grid-area: 5 / 2 / 9 / 6;
    }

    .AboutSection_Img {
        width: 100%;
        height: 100%;
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
        font-size: 1.5rem;
        line-height: 1.7;
    }

    .MainParagraph {
        color: var(--white-b);
        font-size: 1.125rem;
        line-height: 1.7;
        font-family: "Jost", sans-serif;
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
        text-transform: uppercase;
        letter-spacing: 1px;
        cursor: pointer;
        z-index: 1;
        position: relative;
        width: fit-content;
        height: fit-content;
        font-family: "Jost", sans-serif;
        text-decoration: none;
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

    @media screen and (max-width: 1439px) {
        
        .AboutSection_Grid {
            grid-template-rows: repeat(7, 1fr);
        }
        
        .AboutSection_ContentWrapper {
            padding: 120px;
            grid-area: 3 / 7 / 6 / 13;
        }

        .AboutSection_Content {
            max-height: fit-content;
        }
    }

    @media screen and (max-width: 1400px) {
        .AboutSection_HeaderWrapper {
            padding: 80px;
        }
    
        .AboutSection_ContentWrapper {
            padding: 80px;
        }

        .AboutSection_Wrapper::after {
            height: calc(50% - 190px);
        }

    }

    @media screen and (max-width: 1130px) {
        .AboutSection_Grid{
            display: flex;
            flex-direction: column;
            grid-template-rows: repeat(8, 1fr);
        }

        .AboutSection_HeaderWrapper {
            padding: 120px;
        }

        .AboutSection_ContentWrapper {
            padding: 120px;
        }

        .AboutSection_Wrapper::after {
            height: calc(50% - 120px);
        }

        .AboutSection_ImageWrapper {
            padding-top: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .AboutSection_Wrapper {
            padding-top: 60px;
        }
    }

    @media screen and (max-width: 950px) {
        .AboutSection_HeaderWrapper, .AboutSection_ContentWrapper {
            padding: 120px 0px;
            align-items: center;
            display: flex;
        }

        .AboutSection_Content, .AboutSection_Header{
            width: 90%;
        }
    }

    @media screen and (max-width: 600px) {
        .AboutSection_Grid {
            padding: 0px;
            align-items: center;
        }

        .AboutSection_ImageWrapper {
            width: 90%;
        }
    }

    @keyframes animBtn {
        0% {
            width: 0%;
        }

        100% {
            width: 100%;
        }
    }

</style>