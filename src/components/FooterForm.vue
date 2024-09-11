<template>
  <div class="footerform-bg">
    <div class="container footerform">
      <img src="../assets/footerform-logo.svg" alt="logo" class="footerform-logo">
      <h1 class="footerform-header">Register Your Details To Gain An Immediate Edge In The Crypto Market</h1>
      <div class="footerform-form">
        <input type="text" placeholder="Your First Name">
        <input type="text" placeholder="Your Last Name">
        <input type="text" placeholder="You email">
        <input type="tel" placeholder="Your mobile phone">
        <button>Submit</button>
      </div>
      <div class="footerform-logosbox">
        <img
          v-for="logo in logos"
          :src="require(`../assets/videoform_logos/${logo}.png`)"
          alt="logo"
          :key="logo"
          >
          <img src="../assets/videoform_logos/secure.svg" alt="logo">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['logos']
}
</script>