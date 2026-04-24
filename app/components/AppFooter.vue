<script setup lang="ts"></script>

<template>
  <footer class="border-t border-black/10 mt-24">
    <div class="mx-auto max-w-7xl px-6 py-10 flex flex-col md:flex-row justify-between gap-6 text-sm">
      <div>
        <p class="font-bold">ROCKASHAKA</p>
        <p class="opacity-60">&copy; {{ new Date().getFullYear() }} All rights reserved.</p>
      </div>
      <div class="flex gap-6">
        <a href="#" class="hover:underline">Instagram</a>
        <a href="#" class="hover:underline">TikTok</a>
        <a href="#" class="hover:underline">Spotify</a>
      </div>
    </div>
  </footer>
</template>
