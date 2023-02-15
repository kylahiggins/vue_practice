<template>

<div class="cakes_division">

    <h2>{{ cake_obj.type }}</h2>
    <p>${{ cake_obj.price }}</p>

</div>


</template>

<style scoped>

.cakes_division{
    height: 100px;
    background-color: pink;
}

</style>

<script setup>

defineProps({

    cake_obj: {
        type: Object,
        required: true
    },
});

</script>