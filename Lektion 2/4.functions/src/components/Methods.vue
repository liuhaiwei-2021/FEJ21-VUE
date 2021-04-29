<template>
  <div class=mb-5>
    <h1 class="display-5">Methods</h1>
    <div>
      <!-- 
        <button class="btn btn-secondary me-2" @click="add()">@click add()</button>
        <button class="btn btn-secondary me-2" v-on:click="add">add</button>
        <button class="btn btn-secondary me-2" v-on:click="add()">add()</button>
        <button class="btn btn-secondary me-2" @click="addWith(2)">addWith</button> 
      -->

      <button class="btn btn-secondary me-2" @click="add">Lägg till</button>
      <button class="btn btn-secondary me-2" @click="sub">Ta bort</button>
    </div>
    <div class="mt-3">Antal: {{ amount }}</div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            amount: 0
        }
    },
    methods: {
        add() { 
            this.amount++ 
        },
        
        addWith(nr) { 
            this.amount += nr 
        },
        
        sub() { 
            if(this.amount > 0)
                this.amount--
        }
    }
};
</script>

<style>
</style>