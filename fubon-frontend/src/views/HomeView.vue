<script setup>
import { useCounterStore } from '@/stores/Pinia/counter'
import { useStore } from '@/stores/Vuex/index';
import { computed } from 'vue'

const storePinia = useCounterStore();
const count = storePinia.count;

const storeVuex = useStore();
const msg = computed(() => storeVuex.state.msg);
</script>

<template>
    <main>
        <!-- <TheWelcome /> -->
        <h1>test pinia's count : {{ count }}</h1>
        <h1>test Vuex's msg : {{ msg }}</h1>
    </main>
</template>
