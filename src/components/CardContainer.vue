<template>
  <section class="card-container">

      <Card 
      v-for="(item, index) in dataArray" :key="`data-${index}`"
      
      :logo="require(`../assets/${imageCard[index].url}`)"
      :title="item.title"
      :mainTime="item.timeframes[statement].current"
      :lastTime="item.timeframes[statement].previous"
      :className="imageCard[index].color"
      />
   
     

  </section>
</template>

<script>
import Card from '@/components/Card.vue'



export default {
    name: 'CardContainer',
    components: {
        Card,
    },

    props: {
        dataArray: Array,
        statement: String
    },

    data() {
        return {
            imageCard: [
                {
                    url: 'icon-work.svg',
                    color: 'work',
                },
                {
                    url: 'icon-play.svg',
                    color: 'play',
                },
                {
                    url: 'icon-study.svg',
                    color: 'study',
                },
                {
                    url: 'icon-exercise.svg',
                    color: 'exercise',
                },
                {
                    url: 'icon-social.svg',
                    color: 'social',
                },
                {
                    url: 'icon-self-care.svg',
                    color: 'self',
                },
            ]
        }
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

@media screen and (max-width: 375px) {
    .card-container {
        width: 100%;
        height: 100%;
        flex-direction: column;
        
    }
}

</style>