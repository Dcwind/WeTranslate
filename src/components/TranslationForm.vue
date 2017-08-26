<template>
  <div id="translationForm">
    <p>translationForm component</p>
    <form @submit="formSubmit">
      <input type="text" v-model="textToTranslate" placeholder="Enter text to be translated">
      <button type="submit" value="Translate"></button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'translationForm',
};
</script>
