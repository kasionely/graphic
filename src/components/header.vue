<template>
  <div class="header">
    <div class="header__container container">
      <div class="header__logo">
        <img src="../assets/images/logo.png" alt="Graphic.kz Logo">
      </div>
      <div class="header__links">
        <div class="header__links-items">
          <div class="header__links-item">
            <a href="#" class="link">Портфолио</a>
          </div>
          <div class="header__links-item">
            <a href="#" class="link">Студия</a>
          </div>
          <div class="header__links-item">
            <a href="#" class="link">Портфолио</a>
          </div>
        </div>
        <div class="header__links-logo">
          <img src="../assets/images/header-right-logo.png" alt="Graphic.kz Figma">
        </div>
      </div>
    </div>
    <HeaderLinks></HeaderLinks>
<!--    <img class="header__bg" src="../assets/images/header-bg.png" alt="Graphic Header Background">-->
  </div>
</template>

<script>
import HeaderLinks from '@/components/header-links.vue';

export default {
  components: {
    HeaderLinks,
  },
  name: 'header',
};
</script>
<style lang="scss">
.header {
  background: $header-bg;
  padding: 32px;

  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
  }

  &__bg {
    position: absolute;
    top: 0;
    right: 40%;
  }

  &__links {
    display: flex;
  }

  &__links-items {
    display: flex;
    margin-right: 30px;
  }

  &__links-item {
    margin: 0 25px;
  }
}
</style>
