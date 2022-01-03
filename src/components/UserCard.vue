<template>
    <section class="user-card">
        <div class="user-info px-30">
            <div class="user-img">
                <img src="../assets/image-jeremy.png" alt="">
            </div>

            <div class="user-info-name">
                <p>Report for</p>
                <h2>Jeremy Robson</h2>
            </div>
        </div>
        <div class="time px-30">
            <ul>
                <li>
                    <button value="daily" @click="$emit('prova', 'daily')" :class="{active: (statement === 'daily')}">Daily</button>
                </li>
                <li>
                    <button value="weekly" @click="$emit('prova', 'weekly')" :class="{active: (statement === 'weekly')}">Weekly</button>
                </li>
                <li>
                    <button value="monthly" @click="$emit('prova', 'monthly')" :class="{active: (statement === 'monthly')}">Monthly</button>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'UserCard',

    props: {
        statement: String,
    }
}
</script>

<style scoped lang="scss">
@import '@/styles/var.scss';

    .user-card {
        margin-left: 15px;
        margin-right: 15px;
        height: 480px;
        width: 250px;
        background-color: $front-card;
        border-radius: 15px;
        box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.262);

        .user-info {
            width: 100%;
            height: 70%;
            background-color: $user-color;
            border-radius: 15px;

            .user-img {
                height: 80px;
                img {
                    height: 100%;
                    margin-top: 30px;
                    border-radius: 100%;
                    border: 3px solid white;
                }
            }

            .user-info-name {
                padding-top: 70px;
                p {
                    font-size: 14px;
                    color: $subtext-color;
                }

                h2 {
                    font-size: 38px;
                    font-weight: 300;
                }
            }
        }

        .time {
            height: 30%;
            ul {
                height: 100%;
                list-style: none;
                display: flex;
                flex-direction: column;
                justify-content: space-evenly;
                padding: 15px 0;

                li {

                    button {
                        background-color: transparent;
                        border: none;
                        color: $subtext-color;
                        font-size: 18px;
                        cursor: pointer;
                        
                        &:active {
                            color: white;
                        }
                    }
                    .active {
                        color: white;
                    }

                }
            }
        }
    }


</style>