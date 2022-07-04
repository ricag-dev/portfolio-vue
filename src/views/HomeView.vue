<script setup lang="ts">
import items from "@/assets/data/portfolio.json";
</script>

<template>
  <main class="container">
    <div class="grid grid-cols-4 gap-4">
      <div class="drop-shadow-lg p-2" v-for="(item, key) in items" :key="key">
        <img
          :src="`/src/assets/img/portfolio/${item.img}`"
          alt=""
          class="relative z-10 object-cover h-48 w-full rounded overflow-hidden"
        />
      </div>
    </div>
  </main>
</template>
