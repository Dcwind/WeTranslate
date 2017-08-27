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
    translateText(text) {
      this.$http.get("https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20170824T042513Z.ee6ff7e10f61b641.6001d15dc0e2ce6bc258eb80692dbb5e4b5d096d&text=`text`&lang=ru")
      .then((response) => {
        console.log(response)
      })
    },
  },
};
</script>



