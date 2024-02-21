<template>
     <div class="shadow border w-full overflow-hidden mb-5 cursor-pointer h-[200px]" >
        <div class="flex h-full">
            <img @click="details" src="assets/iphone15.jpg" alt="iphone 15 pro max" class="h-full"  width="200px">
            <div class="p-4 flex flex-col">
                <div>
                    <h1 class="text-2xl text-sky-300">Iphone 15 Pro Max</h1>
                    <p class="text-gray-400">
                        this is the latest phone from apple commpany
                    </p>
                </div>
                <h1 class="mt-auto text-xl text-white">$1850.99</h1>
            </div>
        </div>
    </div>
  
</template>

<script setup>
const name = ref("");
const id  = ref("");


const details = () =>{
    navigateTo(`/phone/${name}-${id}`);
    // navigateTo(`/phone/${name.value}-${id.value}`);
}

</script>

<style>

</style>