<template>
  <div id="translationForm">
    <p>translationForm component</p>
    <form @submit.prevent="formSubmit">
      <input type="text" v-model="textToTranslate" placeholder="Enter text to be translated">
      <button type="submit" >Translate</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'translationForm',
  data() {
    return {
      textToTranslate: '',
    };
  },
  methods: {
    formSubmit() {
      this.$emit('formSubmit', this.textToTranslate);
    },
  },
};
</script>
