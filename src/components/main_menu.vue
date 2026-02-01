<template>
    <slot>asd</slot>
  <section class="d-flex justify-sm-space-around align-center mx-auto">
    <div>  <v-btn @click="toggleTheme">
      تغییر تم
    </v-btn></div>

    <div class="main_menu ">
      <v-btn variant="text">
        Button
      </v-btn>
      <v-menu>
        <template #activator="{ props }">
          <v-btn
            color=""
            v-bind="props"
          >
            Activator slot
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            :value="index"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-btn variant="text">
        Button
      </v-btn>
      <v-btn variant="text">
        Button
      </v-btn>
      <v-btn variant="text">
        Button
      </v-btn>
      <v-btn variant="text">
        Button
      </v-btn>
    </div>

    <div class="main_icon">
      <v-img
        aspect-ratio="1/1"
        cover
        src="/src/assets/diamond.png"
        :width="80"
      />

    </div>
  </section>

  <v-sheet class="mx-auto" width="300">
    <v-form fast-fail @submit.prevent="submit_func">
      <v-text-field
        v-model="firstName"
        label="First name"
        :rules="firstNameRules"
      />

      <v-text-field
        v-model="lastName"
        label="Last name"
        :rules="lastNameRules"
      />

      <v-btn block class="mt-2" type="submit">Submit</v-btn>
    </v-form>
  </v-sheet>

</template>

<script setup lang="ts">
  import { useTheme } from 'vuetify'
  const emit = defineEmits(['username'])
  const theme = useTheme()
  const items: any[] = []

  function submit_func () {
    emit ('username', firstName.value + lastName.value)
  }

  function toggleTheme () {
    theme.global.name.value
      = theme.global.current.value.dark ? 'light' : 'dark'
  }

  const firstName = ref('')
  const firstNameRules = [
    (value: string | any[]) => {
      if (value?.length >= 3) return true
      return 'First name must be at least 3 characters.'
    },
  ]

  const lastName = ref('123')
  const lastNameRules = [
    (value: string) => {
      if (/[^0-9]/.test(value)) return true
      return 'Last name can not contain digits.'
    },
  ]

</script>

<style>
 section{
    height: 20vh;
    width: 95vw;
    background-color: rgb(88, 88, 88);

 }
</style>
