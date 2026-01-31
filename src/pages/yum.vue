<script setup lang="ts">
  const emit = defineEmits(['save'])

  function submit () {
    emit('save')
  }

</script>

<template>
  <button @click="submit">Save</button>

</template>
