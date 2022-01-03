<template>
    <section class="user-card">
        <div class="user-info px-30">
            <div class="user-img">
                <img src="../assets/image-jeremy.png" alt="">
            </div>

            <div class="user-info">
                <p>Report for</p>
                <h2>Jeremy Robson</h2>
            </div>
        </div>

        <div class="time">

        </div>
    </section>
</template>




<script>
export default {
    name: 'UserCard'
}
</script>

<style scoped lang="scss">
@import '@/styles/var.scss';

    .user-card {
        height: 500px;
        width: 250px;
        background-color: $front-card;
        border-radius: 15px;
        box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.262);

        .user-info {
            width: 100%;
            height: 65%;
            background-color: $user-color;
            border-radius: 15px;

            .user-img {
                height: 80px;
                img {
                    height: 100%;
                    margin-top: 30px;
                    border-radius: 100%;
                    border: 2px solid white;
                }
            }

            .user-info {
                padding-top: 60px;
                p {
                    font-size: 14px;
                    color: $subtext-color;
                }

                h2 {
                    font-size: 40px;
                    font-weight: 300;
                }

            }

        }
    }


</style>