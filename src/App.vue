<template>
  <main>
    <UserCard />


  </main>
  



</template>

<script>
import UserCard from '@/components/UserCard.vue'

export default {
  name: 'App',
  components: {
    UserCard

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

</style>
