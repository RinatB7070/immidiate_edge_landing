<template>
  <section class="container">
    <div class="rich-people_box">
      <div v-for="people in peopleData" class="rich-people" :key="people"> 
        <img :src="require(`../assets/${people.img}.png`)" alt="portrait">
        <div class="rich-people__content_box">
          <h1>{{ people.name }}</h1>
          <span>{{ people.title }}</span>
          <p>“{{ people.quote }}“</p>
        </div>
      </div> 
    </div> 
  </section>
</template>

<script>
export default {
  data () {
    return {
      peopleData: [
        {
          img: 'bill',
          name: 'Bill Gates',
          title: 'Crypto Investor',
          quote: 'Crypto is the fastest way to earn instant cash in today’s market if you know where to look. Massive earnings and growth in the hundreds even thousands of percent are up for grabs to those who have the tools to take action!'
        },
        {
          img: 'twins',
          name: 'Winklevoss twins',
          title: 'Bitcoin Billionares',
          quote: 'Buy low, sell high, its that simple. Crypto currency is the future of rapid growth and earning potential. You don’t need to be a wall street expert to gain the competitive advantage needed to benefit from this 500 Billion Dollar market.'
        }
      ]
    }
  }
}
</script>