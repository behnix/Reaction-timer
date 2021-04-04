<template>
  <p>Your Reaction Time: {{score}}ms</p>
  <p class="rank"> You are {{ rank }}</p>
</template>

<script>
export default {
props:['score'],
data(){
    return{
        rank:null
    }
},
mounted(){
    if (this.score < 250){
        this.rank = 'Ninja finger'
    }else if (this.score < 400) {
        this.rank = 'Rapid Reflexes'
    }else{
        this.rank = 'Snail pace'
    }
}
}
</script>

<style>
.rank{
    width: 400px;
    background-color:#0faf87;
    padding: 100px 0;
    margin: 40px auto;
    color: white;
    border-radius: 20px;
    text-align: center;
    font-weight: 800;
}
</style>