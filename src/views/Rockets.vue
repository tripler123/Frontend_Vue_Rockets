<template>
  <Section>
      <new-rocket-form></new-rocket-form>
      <rocket-list  class="mt-3"></rocket-list>
  </Section>
</template>

<script>
import NewRocketForm from "../components/NewRockeForm.vue";
import RocketList from '../components/RocketsList.vue';

export default {
    name: 'rockets',
    components:{
        NewRocketForm,
        RocketList
    },
    
    async mounted() {
       this.$store.dispatch('getRockets')
    },
};
</script>

<style>
</style>
