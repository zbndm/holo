<template>
  <section class="holodos-start">
    <Loading v-if="loading" />
    <div class="holodos-start-item" v-else>
      <img src="img/logo-app.webp" loading="lazy" alt="Холодос" width="200" />
      <nuxt-link class="button holodos-start-btn square_btn" to="/catalog">
        Відкрити холодос
      </nuxt-link>
      <p>бот агрегує товари із бази користувачів та мереж супермаркетів</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      loading: true
    };
  },

  mounted() {
    Telegram.WebApp.BackButton.hide();
    Telegram.WebApp.MainButton.hide();
    this.loading = false;
  }
};
</script>

<style scoped>
img {
  margin-bottom: 15px;
}
</style>
