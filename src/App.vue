<script setup>
import MyBar from './components/MyBar.vue';
import MyCard from './components/MyCard.vue';
import items from './attractions.json';
</script>

<template>
  <header>
    <MyBar />
  </header>

  <main>
    <h1 style="padding: 10px;"></h1>
    <div className="grid-container">
      <MyCard v-bind="items[0]"/>
      <MyCard v-bind="items[1]"/>
      <MyCard v-bind="items[2]"/>
      <MyCard v-bind="items[3]"/>
      <MyCard v-bind="items[4]"/>
      <MyCard v-bind="items[5]"/>
      <MyCard v-bind="items[6]"/>
      <MyCard v-bind="items[7]"/>
      <MyCard v-bind="items[8]"/>
      <MyCard v-bind="items[9]"/>
    </div>
  </main>
</template>

<style scoped>
  .grid-container{
    display: grid;
    grid-column-gap: 0.5rem;
    grid-row-gap: 0.5rem;
  }

  @media (min-width: 400px){
    .grid-container {grid-template-columns: repeat(2, 1fr);}
  }
  @media (min-width: 601px){
    .grid-container {grid-template-columns: repeat(3, 1fr);}
  }
  @media (min-width: 1023px){
    .grid-container {grid-template-columns: repeat(5, 1fr);}
  }
</style>
