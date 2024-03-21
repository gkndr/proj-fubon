<script setup>
import { useCounterStore } from '@/stores/Pinia/counter'

// import { useStore } from '';
import { computed, onMounted } from 'vue'

const storePinia = useCounterStore();
const count = storePinia.count;

// const storeVuex = useStore();
// const msg = computed(() => storeVuex.state.msg);

onMounted(() => {
  const handleButtonClick = (evt) => {
    //get target
    const button = evt.target;
    console.log("event touch", button)
    console.log("按鈕被點擊了");


  }
})

</script>

<template>
  <main>
    <!-- <TheWelcome /> -->
    <h1>test pinia's count : {{ count }}</h1>
    <!-- <h1>test Vuex's msg : {{ msg }}</h1> -->

    <button id="myButton">Test</button>
  </main>


</template>
