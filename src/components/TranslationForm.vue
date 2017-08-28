<template>
  <div id="translationForm">
    <p>translationForm component</p>
    <form @submit.prevent="formSubmit">
      <input type="text" v-model="textToTranslate" placeholder="Enter text to be translated">
      <select v-model="lang">
        <option value="ru">Russian</option>
        <option value="fr">French</option>
        <option value="zh">Chinese</option>
        <option value="es">Spanish</option>
      </select>
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
      lang: '',
    };
  },
  methods: {
    formSubmit() {
      this.$emit('formSubmit', this.textToTranslate);
    },
  },
};
</script>
