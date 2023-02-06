<script setup>
const route = useRoute()

useHead({
    title: capitalizeFirstLetter(route.params.name)
})

definePageMeta({
    layout: "custom"
})

function capitalizeFirstLetter(string) {
    return string.charAt(0).toUpperCase() + string.slice(1);
}</script>


<template>
    <div>

        <CarDetailHero />
        <CarDetailAttribute />
        <CarDetailDescription />
        <CarDetailContact />

    </div>
</template>