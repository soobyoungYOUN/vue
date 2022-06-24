<template>
    <div class="result-box">
        <p class="title">윤수01 후보 득표성향 분석</p>
        <div class="table" v-for="age in ages" :key="age.name">
            <AgesRowsView 
                :name="age.name" 
                :percentage="age.percentage" 
                :className="age.className"/>
        </div>
    </div>
</template>
<script>
import AgesRowsView from '@/components/AgesRows.vue';

export default {
    components: {
        AgesRowsView
    },
    data() {
        return {
            ages: [
                {name: "10대", percentage: "0 (0%)", className: "bar-0"},
                {name: "20대", percentage: "8 (10%)", className: "bar-10"},
                {name: "30대", percentage: "16 (20%)", className: "bar-20"},
                {name: "40대", percentage: "8 (10%)", className: "bar-10"},
                {name: "50대", percentage: "9 (11%)", className: "bar-11"},
                {name: "60대", percentage: "11 (13%)", className: "bar-13"},
                {name: "70대", percentage: "10 (12%)", className: "bar-12"},
                {name: "80대", percentage: "13 (16%)", className: "bar-16"},
                {name: "90대", percentage: "4 (5%)", className: "bar-5"},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.result-box {
    width: 100%;
    border: solid 1px black;
    text-align: left;
    padding: 15px;
    .title {
        display: inline-block;
        margin: 15px;
        width: 400px;
    }
    .table {
    }
}
</style>
