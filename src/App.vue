<template>
  <div id="app">
    <h4>WeTranslate</h4>
    <TranslationForm @formSubmit="translateText"></TranslationForm>
  </div>
</template>

<script>
import TranslationForm from './components/TranslationForm';

export default {
  name: 'app',
  components: {
    TranslationForm,
  },
  methods: {
    translateText() {
      
    }
  }
};
</script>



