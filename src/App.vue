<template>
<div class="home">
  <div class="count">
    {{storeCounter.count}}
  </div>
  <div class="buttons">
    <button @click="storeCounter.decreaseCount">-</button>
    <button @click="storeCounter.increaseCount">+</button>
  </div>
  <hr>
  <div>
    Это {{storeCounter.oddOrEven}} число
  </div>
  <hr>
  <div>
    <h3>Edit counter: </h3>
    <input type="number" v-model="storeCounter.count">
  </div>

</div>

</template>


<script setup>

import {useCounterStore} from '@/stores/counter'

const storeCounter = useCounterStore()


</script>


<style>
.home{
  text-align: center;
}
.count{
  font-size: 60px;
  margin: 20px;
}

.buttons button{
  font-size: 40px;
  margin: 5px;
}
</style>
