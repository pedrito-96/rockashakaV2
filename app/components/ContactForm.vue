<script setup lang="ts">
const form = reactive({ name: '', email: '', message: '' })
const sent = ref(false)

function submit() {
  // TODO: wire to /api/contact
  sent.value = true
}
</script>

<template>
  <form class="max-w-xl space-y-5" @submit.prevent="submit">
    <div>
      <label class="block text-sm mb-1">Name</label>
      <input v-model="form.name" required class="w-full border border-black/20 px-4 py-2">
    </div>
    <div>
      <label class="block text-sm mb-1">Email</label>
      <input v-model="form.email" type="email" required class="w-full border border-black/20 px-4 py-2">
    </div>
    <div>
      <label class="block text-sm mb-1">Message</label>
      <textarea v-model="form.message" rows="5" required class="w-full border border-black/20 px-4 py-2" />
    </div>
    <button
      type="submit"
      class="px-6 py-3 bg-black text-white font-semibold hover:bg-neutral-800 transition"
    >
      Send
    </button>
    <p v-if="sent" class="text-green-700 text-sm">Message sent.</p>
  </form>
</template>
