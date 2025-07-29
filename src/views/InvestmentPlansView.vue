<template>
  <div>
    <h1>Investment Plans</h1>
  </div>
  <TopInvestors/>
</template>

<script>
import TopInvestors from '@/components/TopInvestors.vue';

export default {
  name: 'InvestmentPlansView',
  components:{
    TopInvestors
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  margin-top: 2rem;
}
</style>
