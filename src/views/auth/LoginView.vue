<script setup>
import { ref } from 'vue'
import LogoCSUCC from '@/assets/logo/logo-csu-cc.png'
import LogoCSUMain from '@/assets/logo/logo-csu-main.png'
import AppLayout from '@/components/AppLayout.vue'
import { emailValidator, requiredValidator } from '@/utils/validators'

const isPasswordVisible = ref(false)

const onSubmit = () => {
  // Handle form submission logic here
  console.log('Form submitted')
}
</script>

<template>
  <AppLayout>
    <template #content>
      <v-row>
        <v-col cols="12" class="mx-auto d-flex flex-column align-center justify-center">
          <div>
            <div class="d-flex align-center justify-center">
              <v-img :src="LogoCSUMain" width="200" height="200" class="mb-5"></v-img>
              <v-img :src="LogoCSUCC" width="200" height="200" class="mb-5"></v-img>
            </div>

            <v-card class="mx-auto pa-4" elevation="8" max-width="600" rounded="lg">
              <v-card-text>
                <v-form @submit.prevent="onSubmit">
                  <v-text-field
                    class="mb-4"
                    label="Email Address"
                    placeholder="Email Address"
                    prepend-inner-icon="mdi-email-outline"
                    variant="outlined"
                    :rules="[requiredValidator, emailValidator]"
                  ></v-text-field>

                  <v-text-field
                    class="mb-4"
                    :append-inner-icon="isPasswordVisible ? 'mdi-eye-off' : 'mdi-eye'"
                    :type="isPasswordVisible ? 'text' : 'password'"
                    label="Password"
                    placeholder="Enter your password"
                    prepend-inner-icon="mdi-lock-outline"
                    variant="outlined"
                    :rules="[requiredValidator]"
                    @click:append-inner="isPasswordVisible = !isPasswordVisible"
                  ></v-text-field>

                  <v-btn
                    class="font-weight-bold"
                    prepend-icon="mdi-login"
                    color="success"
                    size="large"
                    block
                    type="submit"
                  >
                    Log In
                  </v-btn>
                </v-form>
              </v-card-text>

              <v-card-text class="text-center">
                <v-btn color="primary" variant="text" text>
                  Sign up now <v-icon icon="mdi-chevron-right"></v-icon>
                </v-btn>
              </v-card-text>
            </v-card>

            <div class="text-center mt-4">
              <v-btn
                class="font-weight-bold"
                color="success"
                size="large"
                variant="elevated"
                text
                to="/"
              >
                Back to Home <v-icon icon="mdi-chevron-left"></v-icon>
              </v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
