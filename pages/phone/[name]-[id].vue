<template>

    <div>        
      <PhoneDetailHero />
      <PhoneDetailAttributes />
      <PhoneDetailDescription />
      <PhoneDetailContact />
    </div>
  
</template>

<script  setup>
   const { toTitleCase } = useUtilities();
   const route =  useRoute();

   
   useHead({
    title : toTitleCase(route.params.name),
   });

    definePageMeta({
        layout: "custom",
    });

</script>

<style>

</style>