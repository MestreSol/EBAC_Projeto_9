<template>
    <div class="lcd">
        <p>{{ displayValue }}</p>
    </div>
</template>

<script>
export default {
    name: 'LCD',
    props: {
        displayValue: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
.lcd {
    background-color: #000;
    color: #0f0;
    font-family: 'Digital-7', sans-serif;
    font-size: 2em;
    padding: 10px;
    border: 2px solid #333;
    border-radius: 5px;
    text-align: right;
}
</style>