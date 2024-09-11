<template>
    <div
      class="peoplepopup__box"
      :class="showPopUp"
      @click="closeModal">
      <div class="peoplepopup__content">
        <p>{{ currentPerson.name }}</p>
        <span>${{ currentPerson.profit }}.00</span>
      </div>
      <div class="peoplepopup__imgbox">
        <img src="../assets/flag.svg" alt="flag" class="imgbox__flag">
        <img :src="require(`../assets/justmade_people/${currentPerson.img}.jpg`)" alt="person" class="imgbox__person">
      </div>
    </div>
</template>

<script>
export default {
  props: ['justMadePeople'],
  data () {
    return {
      isActive: true,
      currentPerson: {
        img: this.justMadePeople[1].img,
        name: this.justMadePeople[1].name,
        profit: this.justMadePeople[1].profit
      },
      counter: 0
    }
  },
  methods: {
    closeModal() {
      this.isActive = true
    },
    async togglePerson() {
        setInterval(() => {
          this.isActive = false;
          this.currentPerson = this.justMadePeople[this.counter]
          this.counter == 7 ? this.counter = 0 : this.counter++;
          setTimeout(() => {
            this.isActive = true;
          }, 2000);
        }, 8000)
    }
  },
  computed: {
    showPopUp() {
      return this.isActive ? ' transition_popup' : ''
    }
  },
  mounted () {
    setTimeout(() => {
      this.togglePerson()
    }, 7000)
  }
}
</script>