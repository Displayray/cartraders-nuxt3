<script setup>
const route = useRoute()
useHead({
    title: `${route.params.make ? capitalizeFirstLetter(route.params.make) : "Cars"} in ${capitalizeFirstLetter(route.params.city)}`
})

function capitalizeFirstLetter(string) {
    return string.charAt(0).toUpperCase() + string.slice(1);
}

definePageMeta({
    layout: "custom",
})
</script>

<template>
    <div>
        <div class="mt-32 flex">
            <CarSidebar />
            <NuxtPage />

        </div>
    </div>
</template>