<script setup>
import CardSolid from '@/views/pages/cards/card-basic/CardSolid.vue'
import CardBasic from '@/views/pages/cards/card-basic/CardBasic.vue'
import CardNavigation from '@/views/pages/cards/card-basic/CardNavigation.vue'

</script>

<template>
  <div>
    <p class="text-3xl mt-1 mb-6 ">
      Reviews
    </p>

    <CardSolid />
    <p>____________________________________________________________________________________________________________________________________________________________________________</p>
    <p class="text-2xl mb-4">
      Trending Places this Week 🔥
    </p>

    <CardBasic />

    <p class="text-2xl mb-6 mt-14">
      Navigation Cards
    </p>

    <CardNavigation />


  </div>
</template>
