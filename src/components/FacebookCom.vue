<template>
  <div class="container fb__box">
    <img src="../assets/facebook/facebook.png" alt="logo" class="fb__logo">
    <p class="fb__time">{{ currentTime }}</p>
    <div v-for="person in facebookPersonData" class="fb__person" :key="person">
      <img :src="require(`../assets/facebook/${person.img}.jpg`)" alt="img" class="fb__person__ava">
      <div class="fb__person__content">
        <h1>{{ person.name }}</h1>
        <img :src="require(`../assets/facebook/${person.stars}.png`)" alt="stars" class="fb__person__stars">
        <p>{{ person.message }}</p>
        <div class="fb__person__links">
          <a href="#" class="fb__person__links__like"><img src="../assets/facebook/thumbs-up.svg" alt="thumbs-up"> Like</a>
          <a href="#" class="fb__person__links__comment"><img src="../assets/facebook/message.svg" alt="message"> Comment</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    let date = new Date();
    return {
      facebookPersonData: [
        {
          img: '1',
          name: 'Joanne Bowyer',
          stars: 'four-stars',
          message: 'I have never traded before, but the Immediate Edge makes it so easy. I never thought I would say this since the crypto world can be so complicated… but you do make it so easy to earn unimaginable amounts!',
        },
        {
          img: '2',
          name: 'Rudy Perkins',
          stars: 'five-stars',
          message: 'This is exactly what I’ve been waiting for! Your educational support and high profiting system has got me hooked for life! Thank you so much',
        },
        {
          img: '3',
          name: 'Clark Ross',
          stars: 'four-stars',
          message: 'On my first day, I’ve made over 900 Dollars so I can truly say… Finally, I found something that delivers great results',
        },
        {
          img: '4',
          name: 'Steven Shuler',
          stars: 'five-stars',
          message: 'Money in my account from day one, still can’t believe it… I love your system and support team is outstanding!',
        }
      ],
      date: date
    }
  },
  computed: {
    currentTime () {
      function addZero(num) {
        return num >= 0 && num <= 9 ? '0' + num : num
      }
      return addZero(this.date.getDate()) + '.' + addZero((this.date.getMonth() + 1)) + '.' + addZero(this.date.getFullYear()) + ', ' + 
      addZero(this.date.getHours()) + ':' + addZero(this.date.getMinutes()) + ':' + addZero(this.date.getSeconds())
    }
  }
}
</script>