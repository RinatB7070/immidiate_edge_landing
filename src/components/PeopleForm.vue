<template>
  <div class="form-people-bg">
    <div class="container form-people__box">
      <div v-for="person in formPeople" class="form-people__person" :key="person">
        <img :src="require(`../assets/form_people/${person.img}.jpg`)" alt="">
        <h1>{{ person.name }}</h1>
        <p>"{{ person.quote }}"</p>
        <span>
          <img src="../assets/flag.svg" alt="flag">
          {{ person.amount }}
        </span>
      </div>
      <AppForm
        style="width: 100%;"
         v-show="!isTabl"
      ></AppForm>
    </div>
    <AppForm v-show="isTabl" style=""></AppForm>
  </div>

</template>

<script>
import AppForm from './AppForm.vue'

export default {
  props: ['formPeople','isMob', 'isTabl'],
  components: {
    AppForm
  }
}
</script>