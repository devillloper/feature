<template>
  <Main_menu @username="user_name">

    <p>{{ namea }}</p>
  </Main_menu>

  <p>{{ namea }}</p>

  <p>salam</p>
  <v-hover v-slot="{ isHovering }">
  {{ isHovering }}
</v-hover>

</template>

<script lang="ts" setup>
  import Main_menu from '@/components/main_menu.vue'

  const namea = ref('')

  function user_name (name: string) {
    namea.value = name
  }

</script>
