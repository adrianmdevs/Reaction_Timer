<template>
  <p>Reaction Time - {{score}} Milliseconds</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props:['score'],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = 'Cat Reflexes!'
        }else if(this.score < 400){
            this.rank = 'Swift enough!!'
        }else{
            this.rank = 'Nice try! Give it a go again!'
        }
    }

}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: blue;
        font-weight: bold;
}

</style>