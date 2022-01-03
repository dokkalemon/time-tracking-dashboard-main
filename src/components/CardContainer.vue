<template>
  <section class="card-container">

      <Card title="Ciao" mainTime="32hrs" lastTime="7hrs"/>
   
     

  </section>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
    name: 'CardContainer',
    components: {
        Card,
    }
}
</script>

<style scoped lang="scss">
.card-container {
    width: 760px;
    height: 480px;
    display: flex;
    flex-wrap: wrap;
}

</style>