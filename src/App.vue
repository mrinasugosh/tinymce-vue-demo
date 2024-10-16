<script setup lang="ts">
import Editor from '@tinymce/tinymce-vue'
import { ref } from 'vue'
const apiKey = import.meta.env.VITE_TINYMCE_API_KEY
const value = ref('Hello <strong>world</strong>')
</script>

<template>
  <Editor :api-key="apiKey" v-model="value" />
  <div v-html="value"></div>
</template>
