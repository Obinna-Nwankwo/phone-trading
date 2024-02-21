<template   class="bg-white">
    <div>
        <div class="mt-32 flex">
            <PhoneSiderBar  />
            <NuxtPage />
        </div>       
    </div>
</template>

<script setup>
    const { toTitleCase } =  useUtilities();
    const route =  useRoute();

    
    useHead({
        title: `${route.params.make ? toTitleCase(route.params.city) : "Phone"} in ${toTitleCase(route.params.city)}`,
    });

    definePageMeta({
        layout: "custom",
    })

</script>