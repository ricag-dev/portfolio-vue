<script setup lang="ts">
import items from "@/assets/data/portfolio.json";
</script>

<template>
  <main class="container m-auto">
    <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
      <div
        class="
          rounded
          overflow-hidden
          shadow
          relative
          hover:shadow-lg hover:scale-125
          transition-all
        "
        v-for="(item, key) in items"
        :key="key"
      >
        <img
          :src="`/src/assets/img/portfolio/${item.img}`"
          alt=""
          class="relative object-cover h-48 w-full"
        />
        <div
          class="
            absolute
            inset-0
            backdrop-blur-md backdrop-brightness-150
            md:backdrop-filter-none
            bg-white bg-opacity-40
            text-white
            flex
            items-end
            p-10
          "
        >
          <span
            :key="key"
            v-for="(skill, key) in item.tecnologies"
            class="mr-2"
          >
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </main>
</template>
