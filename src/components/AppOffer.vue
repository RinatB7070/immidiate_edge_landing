<template>
  <section class="offer-bg">
    <div class="container offer" id="header-margin">
      <h1 class="offer__header">Make $950 To $2200 Daily With The World’s Most Intelligent Crypto Software</h1>
      <div class="offer_videoform_box">
        <video src="../assets/add.mp4" controls autoplay loop muted playsinline></video>
        <AppForm :style="formStyle"></AppForm>
      </div>
      <div class="offer__logos_box">
        <img
          v-for="logo in logos"
          :src="require(`../assets/videoform_logos/${logo}.png`)"
          alt="logo"
          :key="logo"
          >
          <img src="../assets/videoform_logos/secure.svg" alt="logo">
      </div>
      <h2>Today is your chance to join us and earn instantly!</h2>
    </div>
  </section>
</template>

<script>
import AppForm from './AppForm.vue'
export default {
  props: ['logos'],
  data () {
    return {
      formStyle: {
        border: '2px solid rgb(126, 211, 33)',
        backgroundColor: 'rgba(0, 0, 0, 0.4)'
      }
    }
  },
  components: {
    AppForm
  }
}
</script>