<template>
  <div class="container">
    <div class="sample-grid">
      <div v-for="number in numbers" :key="number" class="aaa12">{{number}}</div>
    </div>  
    <div class="sample-flex">
      <div v-for="number in numbers" :key="number" class="aaa12">{{ number }}</div>
    </div>
    <div class="calendar">
      <div class="sample-flex">
        <div v-for="number in numbers7" :key="number" class="aaa12">{{number}}</div>
      </div>
      <div class="sample-flex">
        <div v-for="number in numbers7" :key="number" class="aaa12">{{number}}</div>
      </div>
      <div class="sample-flex">
        <div v-for="number in numbers7" :key="number" class="aaa12">{{ number }}</div>
      </div>
      <div class="sample-flex">
        <div v-for="number in numbers7" :key="number" class="aaa12">{{ number }}</div>
      </div>
      <div class="sample-flex">
        <div>
          <div v-for="number in numbers7" :key="number" class="aaa12">{{ number }}</div>
        </div>
      </div>
    </div>
  </div>

</template>

<script lang="ts">
import Vue from "vue";
import "../css_style/clonstyle.css";
import { ref } from "vue";
export default Vue.extend({
  setup() {
    const numbers = ref(Array.from({ length: 30 }, (_, index) => index + 1));
    const numbers7 = ref(Array.from({ length: 7 }, (_, index) => index + 1));
    return {
      numbers,
      numbers7
  }
  }

});

</script>

<style scoped>
.sample-grid {
  display: grid;
  background-color: wheat;
  grid-template-columns: repeat(7, 50px);
  /* grid-template-columns: 200px 1fr */
  /* grid-template-columns: 1fr 10px 10px 10px */
  /* grid-template-columns: 20px 1fr 1fr 10px; */
  gap: 10px;
}
.sample-flex {
  display: flex;
  background-color: aquamarine;
  gap: 20px;
}
</style>