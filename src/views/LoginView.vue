<script setup lang="ts">
import { ref } from "vue";

const form = ref({
  email: "",
  password: "",
  remember: false,
});

const rules = [
  (value: string) => {
    if (value) return true;
    return "You must enter a first name.";
  },
];

const submit = () => {
  alert(JSON.stringify(form.value));
};
</script>

<template>
  <v-row justify="center">
    <v-col cols="4">
      <v-card class="pa-4">
        <v-card-title class="text-center">Login Here</v-card-title>
        <v-card-item>
          <v-form @submit.prevent="submit">
            <v-text-field
              v-model="form.email"
              variant="solo"
              prepend-inner-icon="mdi-mail"
              :rules="rules"
              label="Name"
            ></v-text-field>
            <v-text-field
              v-model="form.password"
              type="password"
              variant="solo"
              prepend-inner-icon="mdi-key"
              label="Password"
            >
            </v-text-field>
            <v-checkbox
              v-model="form.remember"
              label="Remember Me"
              color="#000"
              hide-details
            ></v-checkbox>
            <v-btn color="red-darken-3" class="mt-2" type="submit" block
              >Submit</v-btn
            >
          </v-form>
        </v-card-item>
        <v-card-action>
          <div class="mx-4">
            <v-btn block to="/register"> Register </v-btn>
          </div>
        </v-card-action>
      </v-card>
    </v-col>
  </v-row>
</template>
