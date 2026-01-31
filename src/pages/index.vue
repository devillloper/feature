<template>
  <Yum @save="onSave" />
  <v-btn variant="tonal">
  Button
</v-btn>
</template>

<script lang="ts" setup>
  import Yum from './yum.vue'
  function onSave () {
    console.log('saved')
  }

  //
</script>
