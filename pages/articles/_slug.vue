<template>
  <div class="modal animated fadeIn" :class="{'is-active': slug}" v-if="slug">
    <div class="modal-background"></div>
    <div class="modal-card animated bounce">
      <header class="modal-card-head">
        <p class="modal-card-title">
          Читать про {{ slug }}
        </p>
        <button class="modal-close is-large" aria-label="close" @click="close"></button>
      </header>
      <section class="modal-card-body content">
        <p class="has-text-left">{{ text }}</p>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ app }) { // тут мы будем скачивать статью по заданному урлу
    const content = await app.$axios.$get('https://baconipsum.com/api/?type=meat-and-filler');
    return {
      text: content[0],
    };
  },
  computed: {
    slug() {
      return this.$route.params.slug;
    },
  },
  methods: {
    close() {
      this.$router.go(-1); // тут можно встроить обработчик, чтобы если пользорватель пришел на эту страницу по SSR, то он попадал на главную
    },
  },
};
</script>
