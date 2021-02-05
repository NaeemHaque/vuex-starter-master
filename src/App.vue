<template>
    <div id="app">
        <compBookListOne></compBookListOne>
        <compBookListTwo></compBookListTwo>
        <button class="btn btn-success" @click="priceReduce">Get tk 5 off</button>
    </div>
</template>

<script> 
import compBookListOne from "./components/BookListOne"
import compBookListTwo from "./components/BookListTwo"
export default {
   
    components:{
      compBookListOne,
      compBookListTwo
    },
    methods: {
        priceReduce(){
            // this.$store.commit('reducePrice');       //changed by using methods:
            this.$store.dispatch('decrasePrice');      //changed by using actions:
        }
    },
}
</script>
