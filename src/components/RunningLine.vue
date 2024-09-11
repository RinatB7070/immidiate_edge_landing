<template>
  <div class="rl-bg">
    <div class="rl">
      <div class="rl-inner">
        <div v-for="person in people_active" class="rl__people" :key="person">
          <img :src="require(`../assets/people/${person.img}.jpg`)" alt="portrait">
          <span class="people__content">
            <span class="people__content__name">{{ person.name }}</span>
            <span class="people__content__money">${{ person.profit }}.00</span>
          </span>
        </div>
      </div>
    </div>
  </div>


</template>

<script>
export default {
  props: ['people'],
  data () {
    return {
      people_active: [
      {
          img: '1',
          name: 'D Ward',
          profit: 547
        },
        {
          img: '2',
          name: 'I Cox',
          profit: 483
        },
        {
          img: '3',
          name: 'J Payne',
          profit: 566
        },
        {
          img: '4',
          name: 'B Sims',
          profit: 289
        },
        {
          img: '5',
          name: 'l Edwards',
          profit: 789
        }
      ]
    }
  },
  methods: {
    moveLine () {
      let counter = 5;
      setInterval(() => {
        this.people_active.push(this.people[counter])
        counter++;
        this.people_active.shift()
        if (counter == this.people.length) {
          counter = 0;
        }
      }, 3000);
    }
  },
  mounted() {
    this.moveLine();
  }
}
</script>