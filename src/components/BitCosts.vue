<template>
  <div class="bit-costs-bg" >
    <div class="container">
      <div  class="bit-costs">
        <div v-for="cost in bitCosts" class="bit-cost" :key="cost">
          <span class="bit-cost__name">{{ cost.name }}</span>
          <span  class="bit-cost__amount">{{cost.amount}}</span>
          <img :src="require(`../assets/plus-${cost.btn}.svg`)" alt="">
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      bitCosts: [
        {
          name: 'BTC',
          amount: '+ 90.60123',
          btn: 'blue'
        },
        {
          name: 'ETH',
          amount: '+ 90.60123',
          btn: 'green'
        },
        {
          name: 'LTC',
          amount: '+ 90.60123',
          btn: 'green'
        },
        {
          name: 'EOS',
          amount: ' + 90.60123',
          btn: 'green'
        },
        {
          name: 'XRP',
          amount: ' + 90.60123',
          btn: 'green'
        },
        {
          name: 'BCH',
          amount: '+ 90.60123',
          btn: 'green'
        },

      ]
    }
  }
}
</script>