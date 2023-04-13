<script setup>
import {Field, Form, ErrorMessage} from 'vee-validate';
import * as yup from 'yup';

function isRequired(value) {
  if (value && value.trim()) {
    return true;
  }
}
const passwordRules = yup.string().required().min(8);

// import TheWelcome from '../components/TheWelcome.vue'
</script>

<template>
  <main>
    <Form>
      <label>
        password
      </label>
      <Field name="password" type="password" :rules="passwordRules" />
      <ErrorMessage name="password" />
    </Form>


    <!--    <TheWelcome />-->
  </main>
</template>
