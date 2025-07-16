<script setup>
import LogoCSUCC from '@/assets/logo/logo-csu-cc.png'
import LogoCSUMain from '@/assets/logo/logo-csu-main.png'
import AppLayout from '@/components/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content>
      <v-row>
        <v-col cols="12" sm="8" class="mx-auto d-flex flex-column align-center justify-center">
          <div class="d-flex align-center justify-center">
            <v-img :src="LogoCSUMain" width="200" height="200" class="mb-5"></v-img>
            <v-img :src="LogoCSUCC" width="200" height="200" class="mb-5"></v-img>
          </div>

          <h1 class="text-h1 text-center my-5 font-weight-bold">Hello Dominic</h1>

          <p class="text-center mb-5">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum fuga at iusto est deserunt
            quibusdam aliquam nostrum odit vitae odio totam labore temporibus, quas quae consectetur
            rerum, quos voluptate dolor! Lorem ipsum dolor, sit amet consectetur adipisicing elit.
            Dolorum provident eius labore molestias libero quas iure, similique dignissimos vitae
            molestiae incidunt! Hic accusantium quisquam similique ratione quibusdam rem atque
            impedit?
          </p>

          <div class="d-flex justify-center">
            <v-btn
              class="font-weight-bold mt-5"
              prepend-icon="mdi-login"
              size="x-large"
              color="success"
              elevation="10"
              to="/login"
            >
              Login Here!
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
