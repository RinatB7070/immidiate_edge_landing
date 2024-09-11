<template>
  <div class="advantages-bg">
    <div class="container">
      <h1 class="advantages__header">Register Today to gain Immediate access to this revolutionary software</h1>
      <h2 class="advantages__subheader">Immediate Edge, Instant Earnings</h2>
      <div class="cards_box">
        <div v-for="card in cardData" class="card" :key="card">
          <img :src="require(`../assets/card/${card.img}.svg`)" alt="icon" class="card__icon">
          <h2 class="card__title">{{ card.title }}</h2>
          <p class="card__text">{{ card.text }}</p>
          <img src="../assets/header-logo.png" alt="logo" class="card__logo">
        </div>
      </div>
      <img src="../assets/card/coins.svg" alt="coins" class="advantages__coins">
      <h1 class="advantages__footer"><span>$1,398,692.00</span> Earned By Members In <span>Russia</span> Up To $126.67 Per Hour</h1>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      cardData: [
        {
          img: '1',
          title: 'Simple & Easy To Use',
          text: 'Immediate Edge installs in seconds on any computer or mobile device. PC, MAC, Android, IOS and more.'
        },
        {
          img: '2',
          title: 'Trusted Performance',
          text: 'Fully automated performance instantly scans all the major exchanges. Zero Risk, Immediate Reward.'
        },
        {
          img: '3',
          title: 'Secure & Private',
          text: 'By Using Blockchain technology we deliver 98.9% success rate to all members of our private group.'
        }
      ]
    }
  }
}
</script>