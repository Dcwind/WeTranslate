<template>
  <div id="translationForm" class="row">
    <div class="col-md-6 col-md-offset-3">
      <form class="form-inline" @submit.prevent="formSubmit">
        <input class="form-control" type="text" v-model="textToTranslate" placeholder="Enter text to be translated">
        <select class="form-control" v-model="lang" value="Select language">
          <option value="ru">Russian</option>
          <option value="fr">French</option>
          <option value="zh">Chinese</option>
          <option value="es">Spanish</option>
        </select>
        <button class="btn btn-primary" type="submit" >Translate</button>
      </form>
    </div>
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
  created() {
    this.lang = 'ru';
  },
  methods: {
    formSubmit() {
      this.$emit('formSubmit', this.textToTranslate, this.lang);
    },
  },
};
</script>
