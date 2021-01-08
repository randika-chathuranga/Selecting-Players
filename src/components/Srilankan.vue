<template>
<div class="m-auto">
  <h1 class="text-2xl text-center text-blue-500 m-10">Sri Lanka Squad</h1>
  <ol>
  <li class="flex justify-between" v-for="(players,index) in Srilanka" :key="players.name">
  <div>
    {{players.number}} 
  </div>
    <button @click="remove(index)">x</button>
  </li>
  </ol>
  
  <form class="mt-10 " @submit.prevent="addPlayer">
  <input class="border-rounded" v-model="newMan" placeholder="Type player name"/>
  <button class="border-rounded bg-gradient-to-r from-red-700 to-pink-500" type="submit">Add Player</button>
  </form>
</div>
</template>

<script>
export default {
    data(){
    return{
      newMan:"Chamara Silva",

      Srilanka: [
        {number:"TM Dilshan"},
        {number:"Kusal Perera"},
        {number:"Kumar Sangakkara"},
        {number:"Mahela Jayawardena"},
        {number:"Chamara Kapugedera"},
        {number:"Angelo Mathews"},
        {number:"Thisara Perera"},
        {number:"Nuwan Kulasekara"},
        {number:"Rangana Herath"},
        {number:"Suranga Lakmal"},
        {number:"Lasith Malinga"},
      ]
    }
  },

  name: 'App',
  methods:{
      
  addPlayer(){
    if (this.newMan != "") {
      this.Srilanka.push({number:this.newMan}); 
      this.newMan = '';
    }
  },

  remove(index) {
    this.Srilanka = this.Srilanka.filter((players,i) => i =! index);
  },
 
  },
  

}
</script>

<style>
    
</style>