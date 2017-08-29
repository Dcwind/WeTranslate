<template>
  <div id="app">
    <h4>WeTranslate</h4>
    <TranslationForm @formSubmit="translateText"></TranslationForm>
    <TranslationOut v-text="translatedText"></TranslationOut>
  </div>
</template>

<script>
import TranslationForm from './components/TranslationForm';
import TranslationOut from './components/TranslationOutput';

export default {
  name: 'app',
  data() {
    return {
      translatedText: '',
    };
  },
  components: {
    TranslationForm,
    TranslationOut,
  },
  methods: {
    translateText(text, lang) {
      this.$http.get(`https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20170824T042513Z.ee6ff7e10f61b641.6001d15dc0e2ce6bc258eb80692dbb5e4b5d096d&lang=${lang}&text=${text}`)
      .then((response) => {
        this.translatedText = response.body.text[0];
      });
    },
  },
};
</script>



