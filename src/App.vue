<template>
  <main>
    <UserCard @prova="provass" :statement="statement"/>
    <CardContainer :dataArray="dataJson" :statement="statement"/>


  </main>
  



</template>

<script>
import UserCard from '@/components/UserCard.vue'
import CardContainer from '@/components/CardContainer.vue'

import data from '@/data/data.json'

export default {
  name: 'App',
  components: {
    UserCard,
    CardContainer,

  },

  created() {
    this.getData()
  },

  data() {
    return {
      dataJson: null,
      statement: 'weekly'
    }
  },

  methods: {
    getData() {
      this.dataJson = data
    },

    provass(dato) {
      this.statement = dato
    }
  }




}
</script>

<style lang="scss">
@import '@/styles/global.scss';

main {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media screen and (max-width: 375px) {
  main {
    flex-direction: column;
    padding: 0px 20px;
    justify-content: flex-start;
    margin-top: 20px;
    height: auto;
    
  }
}

</style>
