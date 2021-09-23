<script>
</script>
  
<section class="HomeSection_Wrapper" id="home">
  <!-- <div class="Home_HeroWrapper">
    <div class="Home_Hero_Image_Wrapper">
      
    </div>
  </div> -->
  <div class="Home_Content">
    <div class="Home_Content_HeaderWrapper" >
      <h1 class="Home_Content_Header">
        start your day <br> with our coffee
      </h1>
    </div>
    <div class="Home_Content_SubHeaderWrapper" >
      <span class="Home_Content_SubHeader">
        An experience to remember
      </span>
    </div>
  </div>
  <!-- <div class="Home_Shape_Wrapper">
    <div class="Home_Shape"></div>
  </div> -->
</section>

<style>

  /* .Home_Shape_Wrapper {
    overflow: hidden;
  }

  .Home_Shape {
    overflow: hidden;
    position: absolute;
    bottom: -400px;
    right: -400px;
    width: 800px;
    height: 800px;
    transform: rotate(
45deg);
    background: var(--white-c);
  } */

  .HomeSection_Wrapper {
    position: relative;
    background: linear-gradient(to top, var(--white-c), #FFFFFF);
    width: 100%;
    height: 100vh;
    overflow: hidden;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* .Home_HeroWrapper, .Home_Hero_Image_Wrapper {
    position: absolute;
    width: 100%;
    height: 100%;
    background: transparent;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  #Home_Hero_Image {
    object-fit:cover;
    width: 100%;
    height: 100%;  

    margin-top: 100px;
    margin-left: 700px;
    filter: blur(8px);

  } */

  .Home_Content {
    z-index: 1;
    position: relative;
    top: -4.6vh;

    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }

  .Home_Content_HeaderWrapper {
    width: fit-content;
    height: fit-content;
    background: transparent;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 35px;
  }

  .Home_Content_SubHeaderWrapper {
    width: fit-content;
    height: fit-content;
    background: transparent;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .Home_Content_Header {
    font-weight: 200;
    font-size: 6.8rem;
    line-height: 110px;
    text-align: center;
    text-transform: uppercase;
    font-family: "Casta", sans-serif;
    font-style: normal;
  }

  .Home_Content_SubHeader {
    text-align: center;
    font-weight: 200;
    font-family: "Josefin Sans", sans-serif;
    text-align: center;
    text-transform: uppercase;
    font-size: 2.2rem;
  }  

  @media screen and (max-width: 1300px) {
    .Home_Content_Header {
      font-size: 6rem;
      line-height: 100px;
    }

    .Home_Content_SubHeader {
      font-size: 2rem;
    }

    /* .Home_Shape {
      bottom: -200px;
      right: -200px;
      width: 400px;
      height: 400px;
    } */

  }

  @media screen and (max-width: 900px) {
    .Home_Content_Header {
      font-size: 5.4rem;
      line-height: 90px;
    }

    .Home_Content_SubHeader {
      font-size: 1.8rem;
    }

    .Home_Content {
      width: 90%;
    }

  }

  @media screen and (max-width: 725px) {

    /* #Home_Hero_Image {
      margin-left: 0px;
    } */
    /* .Home_Shape {
      width: 0px;
      height: 0px;
    } */

    .Home_Content_Header {
      font-size: 4rem;
      line-height: 70px;
    }

    .Home_Content_SubHeader {
      font-size: 1.4rem;
    }
  }

  @media screen and (max-width: 560px) {
    .Home_Content_Header {
      font-size: 3rem;
      line-height: 60px;
    }

    .Home_Content_HeaderWrapper {
      margin-bottom: 20px;
    }

    .Home_Content_SubHeader {
      font-size: 1.1rem;
    }
  }

  @media screen and (max-height: 760px) {
    .Home_Content {
      top: 0px;
    }
  }

</style>