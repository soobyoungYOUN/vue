<template>
    <div class="result-box">
        <p class="title">후보별 득표율</p>
        <div class="table" v-for="candi in candidates" :key="candi.name">
            <CandidatesRowsView 
                :name="candi.name" 
                :percentage="candi.percentage" 
                :className="candi.className"/>
        </div>
    </div>
</template>
<script>
import CandidatesRowsView from '@/components/CandidatesRows.vue';

export default {
    components: {
        CandidatesRowsView
    },
    data() {
        return {
            candidates: [
                {name: "1. 윤수01", percentage: "148 (29%)", className: "bar-29"},
                {name: "2. 윤수02", percentage: "108 (21%)", className: "bar-21"},
                {name: "3. 윤수03", percentage: "19 (15%)", className: "bar-15"},
                {name: "4. 김철수", percentage: "166 (33%)", className: "bar-33"},
                {name: "5. 김춘배", percentage: "0 (0%)", className: "bar-0"},
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
        width: 200px;
    }
    .table {
    }
}
</style>
