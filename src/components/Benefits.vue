<script>
let id = 0;
export default {
  data() {
    return {
      benefits: [
        {
          id: id++,
          logo: "passions",
          title: "Indulge your passions",
          text: "Your passions shouldn't be just for the weekend. Earn a living doing what you love."
        },
        {
          id: id++,
          logo: "financial-freedom",
          title: "Gain financial freedom",
          text: "Start making money work for you. There’s nothing quite like earning while you sleep."
        },
        {
          id: id++,
          logo: "lifestyle",
          title: "Choose your lifestyle",
          text: "Own your daily schedule. Fancy a lie-in? Go for it! Take charge of your week."
        },
        {
          id: id++,
          logo: "work-anywhere",
          title: "Work from anywhere",
          text: "Selling online means not being pinned down. Want to work AND travel? Go for it!"
        },
      ]
    }
  }
}
</script>

<template>
  <div class="list-container">
    <div v-for="benefit in benefits" :key="benefit.id" class="list-item">
      <div>
        <img v-if="benefit.logo === 'passions'" src="../assets/illustration-passions.svg"/>
        <img v-if="benefit.logo === 'financial-freedom'" src="../assets/illustration-financial-freedom.svg"/>
        <img v-if="benefit.logo === 'lifestyle'" src="../assets/illustration-lifestyle.svg"/>
        <img v-if="benefit.logo === 'work-anywhere'" src="../assets/illustration-work-anywhere.svg"/>
      </div>
      <div class="text">
        <h3>{{benefit.title}}</h3>
        <p>{{benefit.text}}</p>
      </div>
    </div>
  </div>
</template>

<style>

  .list-container {
    margin-top: 144px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .list-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 24px;
    margin-right: 24px;
  }

  .list-item img {
    width: 124px;
    height: 120px;
    padding: 24px;
    background-color: var(--color-light-blue);
    border-radius: 45px;
    margin-bottom: 32px;
  }

  .list-item h3 {
    font-weight: 800;
    font-size: 18px;
    line-height: 25px;
  }

  .list-item p {
    margin-top: 11px;
    margin-bottom: 56px;
  }

  .list-item .text {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  @media (min-width:480px) {
    .list-item {
      flex-direction: row;
      max-width: 515px;
    }

    .list-item .text {
      align-items: flex-start;
      margin-left: 55px;
    }

    .list-item .text p {
      text-align: left;
    }

    .list-item:nth-child(odd) {
      position: relative;
      left: 20px;
    }
    
    .list-item:nth-child(even) {
      position: relative;
      left: -20px;
    }
  }

  @media (min-width: 769px) {
    .list-container {
      flex-direction: row;
      justify-content: center;
    }

    .list-item {
      flex-direction: column;
      max-width: 255px;
      align-items: flex-start;
    }

    .list-item .text {
      margin: 0px;
    }

    .list-item img {
      width: 160px;
      height: 164px;
    }

    .list-item:nth-child(odd) {
      position: relative;
      left: 0px;
      top: -20px
    }
    
    .list-item:nth-child(even) {
      position: relative;
      left: 0px;
      top: 20px
    }
  }
</style>