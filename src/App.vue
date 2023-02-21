<template>
  <input v-model="a">
  <input v-model="b">
  <p>{{pgdcx}}</p>
  <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <g fill="black"
  x="10">
  <rect width="100" height="100"/>
  </svg>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      a:21,
      b:15,
      n:2
    };
  },
  methods: {
    range(k) {
      let result = Array(k);
      for (let i = 0; i < k; i++) {
        result[i] = i;
      }
      return result;
    },
  },
  computed: {
    pgdcx(){
      let a = this.a;
      let b = this.b;
      let n = this.n;
      let pgdcs=[]

      for (let i=0; i < n; i++){
        if (a > b){
          pgdcs.push((100/a)*b)
           b = a - b
        }
        else {
          a = b
        }
      }
      return pgdcs
    },
    pgdc_y(){

    }

  },
}
</script>

<style>
#app {
  background:blue
}
</style>
