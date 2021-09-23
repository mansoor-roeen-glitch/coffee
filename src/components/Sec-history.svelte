<script>
</script>

<section class="HistorySection_Wrapper" id="History">
    <div class="HistorySection_Grid">
        <div class="HistorySection_HeaderWrapper">
            <div class="HistorySection_Header">
                <h2 class="MainHeading">History</h2>
                <h3 class="SecondaryHeading">Since 1975, we build the brand of our restaurant around the idea of authentic traditional Italian food from the best quality products.</h3>
            </div>
        </div>
        <div class="HistorySection_ContentWrapper">
            <div class="HistorySection_Content">
                <p class="MainParagraph">Our restaurant was established in 1975. Its founder and first chef was Pietro Savastano. Eccentric men with passion for the italian food and italian way of life. His goal was to create a family place with original, traditional food and an informal atmosphere. Years have passed, but we still value the same things and we are proud of it.</p>
                <a class="MainButton" href="/">Learn more</a>
            </div>
        </div>
        <div class="HistorySection_ImageWrapper">
            <div class="HistorySection_Image">
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img class="HistorySection_Img" id="HistorySection_Img" alt="Coffee shop image" src="/images/History.png">
            </div>
        </div>
    </div>
</section>

<style>

    .HistorySection_Wrapper {
        width: 100%;
        height: fit-content;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .HistorySection_Wrapper::before {
        content: "";
        position: absolute;
        top: 50%;
        left: 0px;
        width: 100%;
        height: 50%;
        background: rgb(22, 25, 26);
        z-index: -1;
    }

    .HistorySection_Grid {
        max-width: 1480px;
        padding: 0px 20px;
        position: relative;
        display: grid;
        grid-template-rows: repeat(8, 1fr);
        grid-template-columns: repeat(12, 1fr);
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

    .HistorySection_HeaderWrapper {
        grid-area: 1 / 1 / 5 / 8;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
    }

    .HistorySection_Header {
        padding: 120px;
    }

    .HistorySection_ContentWrapper {
        grid-area: 5 / 1 / 9 / 8;
        display: flex;
        -webkit-box-pack: center;
        justify-content: center;
        background: rgb(22, 25, 26);
    }

    .HistorySection_Content {
        padding: 120px;
    }

    .HistorySection_ImageWrapper {
        grid-area: 2 / 9 / 8 / 14;
    }

    .HistorySection_Image {
        position: relative;
        overflow: hidden;
        max-width: 480px;
        max-height: 720px;
        width: 100%;
    }

    .HistorySection_Img {
        width: 100%;
    }

    @media screen and (max-width: 1425px) {
        .HistorySection_Content, .HistorySection_Header{
            padding: 120px 0px 120px 80px;
        }
    }

    @media screen and (max-width: 1250px) {

        .HistorySection_Wrapper::before {
            background: var(--white-b);
        }

        .HistorySection_ImageWrapper {
            display: none;
        }

        .HistorySection_Content, .HistorySection_Header{
            padding: 80px;
        }

        .HistorySection_ContentWrapper{
            grid-area: 5 / 1 / 9 / 14;
        }

        .HistorySection_HeaderWrapper {
            grid-area: 1 / 1 / 5 / 14;
        }
    }

    @media screen and (max-width: 950px) {
        .HistorySection_Grid {
            display: flex;
            flex-direction: column;
        }

        .HistorySection_Header, .HistorySection_Content {
            width: 90%;
            padding: 80px 0px!important;
        }
    }

    @media screen and (max-width: 600px) {
        .HistorySection_Grid {
            padding: 0px;
            align-items: center;
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