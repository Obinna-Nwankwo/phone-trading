<template>
    <div class="font-serif w-['1000px'] text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto" >
        <input type="text" :class="cityError ? 'outline-2 outline-red-500' : '' " class="py-2 px-8 w-full text-2xl rounded-full rounded-r-none focus:outline-none text-black"  placeholder="Search by name.."  v-model="city">
        <button class="bg-sky-800 hover:bg-sky-700 px-10 py-2" @click="handleSearch">Search</button>
    </div>
</template>

<script setup lang="ts">
    const city = ref("");
    const cityError = ref(false);

    const handleSearch  = () => {
        if (!city.value) {
            return cityError.value = true;
        }
        navigateTo(`/city/${city.value}/phone`);
    }


</script>