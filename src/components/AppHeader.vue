<template>
  <header class="header">
    <div class="header__logo">
      <img src="../assets/header-logo.png" alt="logo">
      <img src="../assets/header-title.png" alt="title">    
    </div>
    <div class="header__cta">
      <div>
        <img src="../assets/flag.svg" alt="flag">
        <p>43</p>
      </div>
      <span>{{ ctaText }}</span>
    </div>
  </header>
</template>

<script>
export default {
  props: ['isMob', 'isTabl'],
  computed: {
    ctaText () {
      return this.isMob ? 'Spots Remaining' : 'Hurry ! Only 43 Spots Left In Russia'
    }
  }
}
</script>