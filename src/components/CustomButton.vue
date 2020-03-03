<template>
<div>
 <button v-bind:key="counter" v-on:click="increment()">Increment</button>
 <label>&nbsp;{{counter}}&nbsp;</label>
 <button v-bind:key="counter" v-on:click="decrement()">Decrement</button>
 </div>


</template>

<script>
export default {
    data() {
        return {
            counter:0
        }
    },
    methods:{
      decrement(){
          if(this.counter>0)
            return this.counter--;
          else
            return this.counter;
      },
      increment(){
            if(this.counter<10)
                return this.counter++;
            else
                alert('You cannot buy more than 10 items')
      }
    }
}
</script>

<style scoped>
    button {
        font-family: 'Avenir', Helvetica, Arial, sans-sarif;
        text-align: center;
        color: #bb0d38a8
    }
</style>