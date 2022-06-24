<template>
    <div class="table-row">
        <div class="name">
            <router-link class="text" to="/result/detail">{{ name }}</router-link>
        </div>
        <div class="rate">
            <img :class="className" src="@/assets/bar.png" />
            {{ percentage }}
        </div>
    </div>
</template>
<script>
export default {
    props: {
        name: String,
        percentage: String,
        className: String
    },
    data() {
        return {
        }
    },
}
</script>
<style lang="scss">
    .table-row {
        width: 90%;
        display: flex;
        .name {
            width: 350px;
            border: solid 1px black;
            text-align: center;
            .text {
              display: block;
              margin-top: 9px;  
            }
        }
        .rate {
            width: 80%;
            border: solid 1px black;
            padding-top: 10px;
            padding-bottom: 5px;
            .bar-33 {
                height: 20px;
                width: 33%;
            }
            .bar-29 {
                height: 20px;
                width: 29%;
            }
            .bar-21 {
                height: 20px;
                width: 21%;
            }
            .bar-16 {
                height: 20px;
                width: 16%;
            }
            .bar-13 {
                height: 20px;
                width: 13%;
            }
            .bar-12 {
                height: 20px;
                width: 12%;
            }
            .bar-11 {
                height: 20px;
                width: 11%;
            }
            .bar-10 {
                height: 20px;
                width: 10%;
            }
            .bar-15 {
                height: 20px;
                width: 15%;
            }
            .bar-5 {
                height: 20px;
                width: 5%;
            }
            .bar-0 {
                height: 20px;
                width: 0%;
            }
        }
    }
</style>