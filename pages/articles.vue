<template>
  <section class="container">
    <div>
      <app-logo/>
      <h1 class="title">
        {{ title }}
      </h1>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <ButtonLinks>
        <nuxt-link class="button--green" :to="{name: 'articles-slug', params: {slug: 'huy'}}">Хуй</nuxt-link>
        <nuxt-link class="button--grey" :to="{name: 'articles-slug', params: {slug: 'gavno'}}">Гавно</nuxt-link>
        <nuxt-link class="button--green" :to="{name: 'articles-slug', params: {slug: 'ant'}}">Муравей</nuxt-link>
      </ButtonLinks>
    </div>
    <router-view></router-view>
  </section>
</template>
<script>
import HomePageMixin from '~/mixins/HomePageMixin.vue';

export default{
  mixins: [HomePageMixin],
  data() {
    return {
      title: 'Список статей',
    };
  },
};

</script>
