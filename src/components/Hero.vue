<script setup>
import IconScroll from "./icons/icon-scroll.vue";
  
</script>

<template>
  <div class="container">
    <img class="mobile-image" src="../assets/illustration-hero-mobile.png"/>
    <div class="not-mobile-image">
      <div>
        <img src='../assets/illustration-hero-left.svg'/>
      </div>
      <div class="squiggle">
        <img src='../assets/bg-footer-squiggle.svg'/>
      </div>
      <div>
        <img src='../assets/illustration-hero-right.svg'/>
      </div>
    </div>
    <text>
      <h1>Get paid for the work you <span>love</span> to do.</h1>
      <p>The 9-5 grind is so last century. We believe in living life on your own terms. Whether you’re looking to escape the rat race or set up a side hustle, we’ve got you covered.</p>
      <IconScroll/>
    </text>
  </div>
</template>

<style>
  .container {
    width: 100%;
    height: 610px;
    margin-top: 65px;
  }

  .mobile-image {
    width: 110%;
  }

  .not-mobile-image {
    display: none;
  }

  text {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 0 24px;
  }

  h1 {
    font-weight: 800;
    font-size: 32px;
    line-height: 40px;
    text-align: center;
    max-width: 245px;
    margin-top: 47px;
  }

  h1 span {
    font-weight: 800;
    color: var(--color-secondary)
  }

  p {
    font-weight: 500;
    font-size: 15px;
    line-height: 25px;
    text-align: center;
    margin-top: 24px;
    margin-bottom: 32px;
    color: var(--color-text-gray)
  }

  @media (min-width:480px) {
    .container {
      height: 460px;
      margin-top: 77px;
    }

    .mobile-image {
      display: none;
    }

    .not-mobile-image {
      display: flex;
      position: absolute;
      justify-content: space-between;
      width: 110%;
      left: -5%;

    }

    h1 {
      margin-top: 34px;
    }

    p {
      max-width: 435px;
    }

    .not-mobile-image div {
      width: 30%;
    }

    .not-mobile-image div img {
      width: 100%;
      height: 360px;
    }

    .not-mobile-image .squiggle img{
      height: 268px;
    }
  }

  @media (min-width: 769px) {
    .container {
      margin-top: 114px;
    }

    h1 {
      font-size: 48px;
      line-height: 56px;
      max-width: 465px;
      margin-top: 70px;
    }

    p {
      max-width: 515px;
    }

    .not-mobile-image div img {
      width: 100%;
      height: 460px;
    }

    .not-mobile-image .squiggle img{
      height: 380px;
    }
  }

</style>