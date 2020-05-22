<template>
    <div>
      <button @click="imcrement">+</button>
      <button v-on:click="decrement">-</button>
      <p><span>{{num}}</span></p>
    </div>
</template>

<script>
    export default {
        name: "Counter",
        props:["num"],
        data(){
          return{
            num:0
          }
        },
      methods:{
          imcrement() {
            //this.num++;
            this.$emit("incre");
          },
          decrement(){
            //this.num--;
            this.$emit("dlcre");
          }
      }
    }
</script>

<style scoped>

</style>
