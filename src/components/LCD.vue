<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
  display: {
    type: String,
    required: true
  }
});
</script>

<template>

    <div class="lcd">
        <h1 class="green">{{ display }}</h1>
    </div>
</template>

<style scoped>

.lcd {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f2f2f2;
    border: 1px solid #ccc;
    border-radius: 10px;
    width: 250px;
    height: 100px;
    margin: 0 auto;
}

h1{
    font-weight: 200;
    font-size: 2.2ch;
    position: relative;
    top: -10px;
    font-family: "Silkscreen", sans-serif;

}
</style>