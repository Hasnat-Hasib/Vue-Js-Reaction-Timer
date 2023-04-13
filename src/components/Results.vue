<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <p>Reaction time- {{ score }} ms</p>
    <p class="rank"> {{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = "Express"
        } else if (this.score < 400) {
            this.rank = "Rapid Reflexes"
        } else {
            this.rank = "Small pace ..."
        }
    }
}
</script>

<style>

</style>