<template>
  <v-hover v-slot="{ isHovering, props }">
    <v-locale-provider rtl>
      <v-list-item href="/consequences/consequences">
        <v-img class="mr-5" height="65" :src="images" width="140" />
      </v-list-item>

      <v-col class="scroll mt-0" :style="`height: calc(100vh - 200px)`">
        <v-divider class="mt-2" />

        <v-list
          v-model:opened="open"
          active-strategy="independent"
          density="default"
          select-strategy="leaf"
        >
          <v-list-group class="mt-2" value="ricks">
            <template #activator="{ props, isOpen }">
              <v-list-item
                active-color="#58586CFF"
                base-color="#181C32"
                :class="
                  isOpen
                    ? 'rounded-lg elevation-0  text-subtitle-2'
                    : 'rounded-lg elevation-0  custom-list-group'
                "
                variant="elevated"
                v-bind="props"
              >
                <template #append="{ isActive }">
                  <v-icon
                    class="mt-1"
                    :icon="isActive ? '' : ''"
                    size="18"
                  />
                </template>
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFF'"
                    icon="mdi-cog"
                    size="24"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >شخصی سازی</span>
                </template>
              </v-list-item>
            </template>
            <v-list-item
              active-color="#A0A9DBFF"
              class="mr-n16"
              style="width: 100%"
              value="Management"
            >
              <v-icon
                :color="'#FFFFFF'"
                icon="mdi-moon-waxing-crescent"
                size="24"
              />
              <span
                class="text-subtitle2 mr-2"
                style="font-size: 13px !important"
              >ارزیابی ریسک</span>
            </v-list-item>
            <v-list-item
              active-color="#58586CFF"
              class="mr-n16"
              href="/toutiya/dashboard/profile"
              value="rickManagement"
            >
              <v-icon :color="'#FFFFFF'" icon="mdi-account" size="24" />
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >اطلاعات شخصی</span>
            </v-list-item>
          </v-list-group>

          <v-divider class="mt-2" />

          <v-list-group class="mt-2" value="2">
            <template #activator="{ props, isOpen }">
              <v-list-item
                active-color="#58586CFF"
                base-color="#181C32"
                :class="
                  isOpen
                    ? 'rounded-lg elevation-0  text-subtitle-2'
                    : 'rounded-lg elevation-0  custom-list-group'
                "
                variant="elevated"
                v-bind="props"
              >
                <template #append="{ isActive }">
                  <v-icon
                    class="mt-1"
                    :icon="isActive ? '' : ''"
                    size="18"
                  />
                </template>
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFF'"
                    icon="mdi-chart-box-outline"
                    size="24"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >عملکرد</span>
                </template>
              </v-list-item>
            </template>
            <v-list-item
              active-color="#A0A9DBFF"
              class="mr-n16"
              href="/toutiya/dashboard/statics?access_level=0"
              style="width: 100%"
              value="Management"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >ابر کاربر</span>
            </v-list-item>
            <v-list-item
              active-color="#58586CFF"
              class="mr-n16"
              href="/toutiya/dashboard/statics?access_level=1"
              value="rickManagement"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >مدیر</span>
            </v-list-item>
            <v-list-item
              active-color="#58586CFF"
              class="mr-n16"
              href="/toutiya/dashboard/statics?access_level=2"
              value="rickManagement"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >سرگروه</span>
            </v-list-item>
          </v-list-group>

          <v-divider class="mt-2" />

          <v-list-group class="mt-2" value="3">
            <template #activator="{ props, isOpen }">
              <v-list-item
                active-color="#58586CFF"
                base-color="#181C32"
                :class="
                  isOpen
                    ? 'rounded-lg elevation-0  text-subtitle-2'
                    : 'rounded-lg elevation-0  custom-list-group'
                "
                variant="elevated"
                v-bind="props"
              >
                <template #append="{ isActive }">
                  <v-icon
                    class="mt-1"
                    :icon="isActive ? '' : ''"
                    size="18"
                  />
                </template>
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFF'"
                    icon="mdi-clipboard-list-outline"
                    size="24"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >طرح</span>
                </template>
              </v-list-item>
            </template>
            <v-list-item
              active-color="#A0A9DBFF"
              class="mr-n16"
              href="/toutiya/dashboard/schemes/scheme-692"
              style="width: 100%"
              value="Management"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >692</span>
            </v-list-item>
            <v-list-item
              active-color="#58586CFF"
              class="mr-n16"
              href="/toutiya/dashboard/schemes/scheme-231"
              value="rickManagement"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >231</span>
            </v-list-item>
            <v-list-item
              active-color="#58586CFF"
              class="mr-n16"
              href="/toutiya/dashboard/schemes/scheme-747"
              value="rickManagement"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >747</span>
            </v-list-item>
            <v-list-item
              active-color="#58586CFF"
              class="mr-n16"
              href="/toutiya/dashboard/schemes/scheme-240"
              value="rickManagement"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >240</span>
            </v-list-item>
          </v-list-group>

          <v-divider class="mt-2" />

          <v-list-group class="mt-2" value="dashboard">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/tasks"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-clipboard-edit-outline"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >وظایف</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="4">
            <template #activator="{ props, isOpen }">
              <v-list-item
                active-color="#58586CFF"
                base-color="#181C32"
                :class="
                  isOpen
                    ? 'rounded-lg elevation-0  text-subtitle-2'
                    : 'rounded-lg elevation-0  custom-list-group'
                "
                variant="elevated"
                v-bind="props"
              >
                <template #append="{ isActive }">
                  <v-icon
                    class="mt-1"
                    :icon="isActive ? '' : ''"
                    size="18"
                  />
                </template>
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFF'"
                    icon="mdi-clipboard-list-outline"
                    size="24"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >تیکت ها</span>
                </template>
              </v-list-item>
            </template>
            <v-list-item
              active-color="#A0A9DBFF"
              class="mr-n16"
              href="/toutiya/dashboard/ticket-service/ticket"
              style="width: 100%"
              value="Management"
            >
              <span
                class="text-subtitle2"
                style="font-size: 13px !important"
              >لیست تیکت ها</span>
            </v-list-item>
          </v-list-group>

          <v-divider class="mt-2" />

          <v-list-group class="mt-2" value="5">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/chat"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-chat-processing-outline"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >گفتگو</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="6">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/organization"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-domain"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >سازمان ها</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="7">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/pattern"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-lock-pattern"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >الگوی رویداد</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="8">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/tnapcy"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-newspaper"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >اخبار برگزیده</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="9">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/ticket-service/ticket"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-chart-box-plus-outline"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >ثبت در پروفایل</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="10">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                href="/toutiya/dashboard/hezarpa"
                style="font-size: 13px !important"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-lightbulb-on-outline"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >تحلیل آسیب پذیری</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>
          <v-list-group class="mt-2" value="10">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                style="font-size: 13px !important"
                to="/vulnerable-analyse"
                value="Home"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-lightbulb-on-outline"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >مدیریت آسیب پذیری</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="11">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#58586CFF"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                style="font-size: 13px !important"
                to="/news-websites"
                value="Home"
                variant="elevated"
              >
                <v-tooltip
                  activator="parent"
                  location="top"
                >مدیریت منابع خبری</v-tooltip>
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-web"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >مدیریت منابع خبری</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="15">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#181C32"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                style="font-size: 13px !important"
                to="/rules"
                value="15"
                variant="elevated"
              >
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-book-open-page-variant"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >مدیریت قوانین</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <v-list-group class="mt-2" value="15">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#181C32"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                style="font-size: 13px !important"
                to="/telegram-management"
                value="15"
                variant="elevated"
              >
                <v-tooltip
                  activator="parent"
                  location="top"
                >مدیریت کانال های تلگرامی</v-tooltip>
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-book-open-page-variant"
                    size="22"
                  />
                </template>
                <template #title>
                  <span
                    class="mr-5"
                    style="font-size: 14px !important"
                  >مدیریت کانال های تلگرامی</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>
          <!-- v-if="irancti_access" -->
          <v-list-group class="mt-2" value="15">
            <template #activator="{ props }">
              <v-list-item
                v-bind="props"
                active-color="#181C32"
                base-color="#181C32"
                class="rounded-lg elevation-0 text-subtitle-2"
                style="font-size: 13px !important;"
                to="/cti"
                value="15"
                variant="elevated"
              >
                <v-tooltip activator="parent" location="top">cti</v-tooltip>
                <template #append="{ isActive }" />
                <template #prepend="{ isActive }">
                  <v-icon
                    :color="isActive ? '#FFFFFF' : '#FFFFFFFF'"
                    icon="mdi-list-box"
                    size="22"
                  />
                </template>
                <template #title>
                  <span class="mr-5" style="font-size: 14px !important;">cti</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group>

          <!-- <v-list-group value="dashboard">
            <template v-slot:activator="{ props }">
              <v-list-item style="font-size: 13px!important;"  base-color="#181C32" v-bind="props"
                active-color="#58586CFF" class="rounded-lg elevation-0 text-subtitle-2" variant="elevated" value="Home">
                <template #append="{ isActive }">
                </template>
                <template #prepend="{ isActive }">
                  <v-icon :color="isActive ? '#FFFFFF' : '#FFFFFFFF'" size="22" icon="mdi-cog"></v-icon>
                </template>
                <template #title>
                  <span class="mr-5">شخصی سازی</span>
                </template>
              </v-list-item>
            </template>
          </v-list-group> -->

          <!-- #181C32 -->
        </v-list>
      </v-col>
    </v-locale-provider>
  </v-hover>
</template>
<script setup lang="ts">
  import axios from 'axios'
  import { onMounted, ref } from 'vue'
  import { useRoute, useRouter } from 'vue-router'
  import image from '@/assets/logo.png'
  import { useApi } from '@/composables/useApi'
  import { getLoginStatus } from '../../pages/entryForm/api/entryFormApi'
  const images = ref(image)

  const route = useRoute()
  const router = useRouter()
  const open = ref<any>()
  const admins = ref<any>([
    ['Management', 'mdi-account-multiple-outline'],
    ['Settings', 'mdi-cog-outline'],
  ])
  const cruds = ref<any>([
    ['Create', 'mdi-plus-outline'],
    ['Read', 'mdi-file-outline'],
    ['Update', 'mdi-update'],
    ['Delete', 'mdi-delete'],
  ])
  const getLoginStatusApi = useApi(getLoginStatus)
  const irancti_access = ref(false)

  async function getLoginStatusFn () {
    await getLoginStatusApi.exec()
    irancti_access.value = getLoginStatusApi?.data?.value?.user?.irancti_access
  }

  onMounted(() => {
    getLoginStatusFn()
  })
</script>
<style>
.custom-list-group:hover {
  background-color: #181c321a !important;
  /* Replace this with your desired hover color */
}
</style>
<style scoped>
.v-list-item__prepend > .v-badge ~ .v-list-item__spacer,
.v-list-item__prepend > .v-icon ~ .v-list-item__spacer,
.v-list-item__prepend > .v-tooltip ~ .v-list-item__spacer {
  width: 15px !important;
}

/* width */
::v-deep(::-webkit-scrollbar) {
  width: 4px !important;
}

/* Track */
::v-deep(::-webkit-scrollbar-track) {
  background: #ffffff00 !important;
}

/* Handle */
::v-deep(.scroll::-webkit-scrollbar-thumb) {
  background: rgba(255, 255, 255, 0.3) !important;
  border-radius: 4px;
}

/* Handle on hover */
::v-deep(::-webkit-scrollbar-thumb:hover) {
  background: #ffffff00 !important;
}

::v-deep(.scroll) {
  width: 100%;
  height: 100%;
  overflow: auto;
  float: right;
}
</style>
