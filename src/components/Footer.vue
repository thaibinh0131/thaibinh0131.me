<script setup lang="ts">
import dayjs from "dayjs";
const year = dayjs().get("year");
</script>

<template>
  <footer class="py-8 px-6">
    <div class="max-w-$md-max-width mx-auto opacity-50 flex">
      <span class="text-sm"> thaibinh0131@{{ year }} </span>
    </div>
  </footer>
</template>
