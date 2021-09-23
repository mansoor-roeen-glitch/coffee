<script>
</script>

<section class="WineSection_Wrapper">
    <div class="WineSection_Grid">
        <div class="WineSection_HeaderWrapper">
            <div class="WineSection_Header">
                <h2 class="MainHeading">Wines</h2>
            </div>
        </div>
        <div class="WineSection_ContentWrapper">
            <div class="WineSection_Content">
                <p class="MainParagraph">We are Sicilians that love the own land so we decided to create our special wine describing local dishes prepared by Sicilian chefs. Taste our self-grown wines, a highlight for wine lovers. We provide fresh, quality grapes for delicious wine to help you enjoy the flavours of this wonderful island.</p>
            </div>
        </div>
    </div>
</section>

<style>

    .WineSection_Wrapper {
        width: 100%;
        height: fit-content;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .WineSection_Grid {
        max-width: 1480px;
        padding: 0px 20px;
        position: relative;
        display: grid;
        grid-template-rows: repeat(3, 1fr);
        grid-template-columns: repeat(12, 1fr);
    }

    .WineSection_HeaderWrapper {
        grid-area: 1 / 1 / 4 / 6;
        padding: 120px;
    }

    .WineSection_ContentWrapper {
        grid-area: 1 / 6 / 4 / 13;
       padding: 120px;
    }

    .MainHeading {
        color: var(--black-b);
        font-family: "Playfair Display", serif;
        font-size: 100px;
        position: relative;
    }

    .MainHeading::before {
        content: "Our";
        position: absolute;
        top: -3rem;
        left: -2rem;
        color: var(--white-b);
        font-size: 60px;
        z-index: -1;
    }

    .MainParagraph {
        color: var(--black-b);
        font-family: "Jost", sans-serif;
        opacity: .9;
        font-size: 1.125rem;
        line-height: 1.7;
    }

    @media screen and (max-width: 1279px) {
        .WineSection_HeaderWrapper, .WineSection_ContentWrapper {
            padding: 80px;
        }

        .WineSection_HeaderWrapper {
            margin-top: 2rem;
            display: flex;
            -webkit-box-pack: center;
            justify-content: center;
        }
    }

    @media screen and (max-width: 1059px) {
        .WineSection_Grid {
            display: flex;
            flex-direction: column;
            width: 90%;
        }

        .WineSection_HeaderWrapper {
            padding-bottom: 60px;
        }

        .WineSection_ContentWrapper {
            padding: 0px 80px 80px
        }
    }

    @media screen and (max-width: 700px) {
        .WineSection_ContentWrapper {
            padding: 0px;
            padding-bottom: 80px;
        }
    }


</style>