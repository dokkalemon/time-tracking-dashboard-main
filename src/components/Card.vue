<template>
  <section class="card">
    <div class="card-container">
        <div class="card-image" :class="className">
            <img :src="logo" alt="">
        </div>
    
        <div class="card-info px-30">
            <div class="card-info-header ">
                <p>{{title}}</p>
                <img src="../assets/icon-ellipsis.svg" alt="">
            </div>
            <div class="card-info-info">
                <div class="card-info-main">
                <h3>{{mainTime}}hrs</h3>
            </div>
            <div class="card-info-subtitle">
                <p>Last Week - {{lastTime}}hrs</p>
            </div>
            </div>
        </div>




    </div>
  </section>
</template>

<script>
export default {
    name: 'Card',
    props: {
        logo: String,
        title: String,
        mainTime: Number,
        lastTime: Number,
        className: String,
    }
}
</script>

<style scoped lang="scss">
@import '@/styles/var.scss';

.card {
    
  height: calc(100% / 2);
  width: calc(100% / 3);
  padding-left: 15px;
  padding-right: 15px;
  position: relative;
  .card-container {
      height: 100%;
      width: 100%;
      background-color: $front-card;
      border-radius: 15px;
      box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.262);
      position: relative;
      overflow: hidden;
      cursor: pointer;
  }
  &:nth-child(-n+3) {
    padding-bottom: 15px;
  }

  &:nth-child(+n+4) {
    padding-top: 15px;
  }

  .card-image {
      width: 100%;
      height: 50px;
      position: relative;
      img {
          height: 140%;
          text-align: left;
          position: absolute;
          right: 20px;
          top: -10px;
      }
  }

  .work {
      background-color: $work-color
  }
  .play {
      background-color: $play-color
  }
  .study {
      background-color: $study-color
  }
  .exercise {
      background-color: $exercise-color
  }
  .social {
      background-color: $social-color
  }
  .self {
      background-color: $self-color
  }

    .card-info {
        width: 100%;
        height: calc(100% - 40px);
        border-radius: 15px;
        background-color: $front-card;
        position: absolute; 
        bottom: 0;
        .card-info-header {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 30px;
            p {
                flex-grow: 1;
            }
            img {
                height: 100%;
                cursor: pointer; 
                &:active {
                    filter: brightness(300%)
                }
            }
        }
       .card-info-info {
           display: flex;
           flex-direction: column;
            .card-info-main {
            margin-top: 25px;
            h3 {
                font-size: 50px;
                font-weight: 300;
            }
        }

        .card-info-subtitle {
            margin-top: 5px;
            p {
                font-size: 14px;
                color: $subtext-color;
            }
        }
       }
    }

    &:active {
        .card-info {
            background-color:  $active-card
        }
    }
}

@media screen and (max-width: 375px) {
.card {
 width: 100%;
 height: 150px;

 margin-top: 20px;
  padding-left: 0px;
  padding-right: 0px;

&:nth-child(-n+3) {
    padding-bottom: 0;
}

  &:nth-child(+n+4) {
    padding-top: 0px;
  }
}


.card-info {
      .card-info-info {
          flex-direction: row !important;
          align-items: center;
          .card-info-main {
              margin-top: 0 !important;
              flex-grow: 1;
              h3 {
                  font-size: 35px !important;
              }
          }
      }
}
}
</style>