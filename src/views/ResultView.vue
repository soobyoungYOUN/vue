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
                {name: "1. 윤수01", percentage: "50 (50%)", className: "bar-50"},
                {name: "2. 윤수02", percentage: "10 (10%)", className: "bar-10"},
                {name: "3. 윤수03", percentage: "10 (10%)", className: "bar-10"},
                {name: "4. 윤수04", percentage: "10 (10%)", className: "bar-10"},
                {name: "5. 윤수05", percentage: "5 (5%)", className: "bar-5"},
                {name: "6. 김철수", percentage: "15 (15%)", className: "bar-15"},
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
