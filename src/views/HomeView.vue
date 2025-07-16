<script setup>
import LogoCSUCC from '@/assets/logo/logo-csu-cc.png'
import LogoCSUMain from '@/assets/logo/logo-csu-main.png'
import AppLayout from '@/components/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content>
      <v-row>
        <v-col cols="12" class="d-flex flex-column align-center justify-center">
          <div class="d-flex align-center justify-center">
            <v-img :src="LogoCSUMain" width="200" height="200" class="mb-5"></v-img>
            <v-img :src="LogoCSUCC" width="200" height="200" class="mb-5"></v-img>
          </div>

          <h1 class="text-h1 text-center mt-16 font-weight-bold">Hello CSU-CC</h1>

          <v-btn
            class="mt-5"
            prepend-icon="mdi-login"
            size="x-large"
            color="success"
            elevation="10"
            to="/login"
          >
            Login Here!
          </v-btn>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>

<style scoped></style>
