<script setup>
import { ref } from 'vue'
import ImgBg from '@/assets/images/img-csu.png'
import LogoCSUText from '@/assets/logo/logo-csu-text.png'

const theme = ref('light')

function onClick() {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}
</script>

<template>
  <v-responsive>
    <v-app :theme="theme">
      <v-app-bar class="px-3">
        <v-app-bar-title>
          <img :src="LogoCSUText" height="60" />
        </v-app-bar-title>

        <v-btn
          :icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          variant="elevated"
          slim
          @click="onClick"
        ></v-btn>
      </v-app-bar>

      <v-main>
        <v-img :src="ImgBg" height="100%" cover>
          <v-container>
            <slot name="content"></slot>
          </v-container>
        </v-img>
      </v-main>
    </v-app>
  </v-responsive>
</template>
