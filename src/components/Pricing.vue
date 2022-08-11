
<template>
  <div class="pricing-container">
    <div class="text">
      <h2>Our pricing plans</h2>
      <p>We only make money when our creators make money. Our plans are always affordable, and it’s completely free to get started.</p>
    </div>
    <div class="cards-container">
      <div class="dip card">
        <img src="../assets/icon-free.svg"/>
        <h3>Dip your toe</h3>
        <p>Just getting started? No problem at all! Our free plan will take you a long way.</p>
        <h1>Free</h1>
        <div class="card-list">
          <p class="check-item">Unlimited products</p>
          <p class="check-item">Basic analytics</p>
          <p class="check-item">Limited marketplace exposure</p>
          <p class="check-item">10% fee per transaction</p>
        </div>
      </div>
      <div class="dive card">
        <img src="../assets/icon-paid.svg"/>
        <h3>Dive right in</h3>
        <p>Ready for the big time? Our paid plan will help you take your business to the next level.</p>
        <h1>$25.00<span>/ month</span></h1>
        <div class="card-list">
          <p class="check-item">Custom domain</p>
          <p class="check-item">Advanced analytics and reports</p>
          <p class="check-item">High marketplace visibility</p>
          <p class="check-item">5% fee per transaction</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style>

  .pricing-container {
    margin-top: 144px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .pricing-container .text {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0 24px;
  }

  .pricing-container h2 {
    font-weight: 800;
    font-size: 24px;
    line-height: 33px;
  }

  .cards-container {
    display: flex;
    flex-direction: column;
  }

  .card {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin: 79px 24px 0px 24px;
    border-radius: 8px;
  }

  .card p {
    text-align: left;
    font-style: normal;
    font-weight: 500;
    font-size: 15px;
    color: white;
  }

  .card h3 {
    font-weight: 800;
    font-size: 18px;
    line-height: 25px;
  }

  .card h1 {
    margin-top: 24px;
    font-size: 40px;
    margin-bottom: 19px;
  }

  .card h1 span {
    font-weight: 500;
    font-size: 15px;
    line-height: 50px;
    color: black;
    bottom: 10px;
    left: 10px;
  }

  .dip {
    background-color: var(--color-light-blue);
    padding: 49px 30px 32px 30px;
    position: relative;
  }

  .dive {
    background-color: var(--color-secondary);
    padding: 61px 30px 32px 30px;
    position: relative;
    color: black;
  }
  .dip img {
    position: absolute;
    top: -20px
  }

  .dive p {
    color: black;
  }

  .dive img {
    position: absolute;
    top: -35px
  }
  .card-list {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .check-item {
    margin: 0px 0px 12px 0px;

  }

  .dip .check-item:before {
      content: "";
      display: block;
      background: url("../assets/icon-check.svg") no-repeat;
      width: 20px;
      height: 10px;
      float: left;
      margin: 8px 6px 0 0;
  }

  .dive .check-item:before {
      content: "";
      display: block;
      background: url("../assets/icon-check-dark.svg") no-repeat;
      width: 20px;
      height: 10px;
      float: left;
      margin: 8px 6px 0 0;
  }

  @media (min-width:480px) {

    .cards-container {
      align-items: center;
    }
    .card {
      max-width: 445px;
    }
  }

  @media (min-width: 769px) {
    .cards-container {
      flex-direction: row;
      justify-content: center;
    }
  }
</style>