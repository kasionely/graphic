<template>
  <div class="header-nav">
    <div class="header-nav container">
      <div class="header-nav__links">
        <div
          :class="{ selected: item.selected }"
          :key="item.type"
          class="header-nav__link"
          v-for="item of links">
          <img
            v-if="item.iconSrc.length"
            class="header-nav__link-icon"
            :src="item.iconSrc"
          >
          <a href="#" class="link">
            {{ item.title }}
          </a>
        </div>
      </div>
      <div class="header-nav__info">

      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'headerNav',
  data() {
    return {
      links: [
        {
          type: 'all',
          iconSrc: '',
          title: 'Все работы',
          selected: true,
        },
        {
          type: 'web',
          iconSrc: require('@/assets/images/icons/computer.svg'),
          title: 'Вэб',
          selected: false,
        },
        {
          type: 'app',
          iconSrc: require('@/assets/images/icons/app.svg'),
          title: 'Приложение',
          selected: false,
        },
        {
          type: 'graphic',
          iconSrc: require('@/assets/images/icons/graphic.svg'),
          title: 'Графика',
          selected: false,
        },
        {
          type: 'smm',
          iconSrc: require('@/assets/images/icons/megaphone.svg'),
          title: 'SMM',
          selected: false,
        },
        {
          type: 'branding',
          iconSrc: require('@/assets/images/icons/star.svg'),
          title: 'Брэндинг',
          selected: false,
        },
        {
          type: 'painter',
          iconSrc: require('@/assets/images/icons/painter.svg'),
          title: 'Цифровая живопись',
          selected: false,
        },
      ],
    };
  },
  methods: {

  },
};
</script>
<style lang="scss">
.header-nav {
  margin-top: 32px;

  &__links {
    display: flex;
    border-bottom: 1px solid rgba($white, 0.1);
    padding: 24px 0;
  }

  &__link {
    display: flex;
    align-items: center;
    margin: 0 12px;
    opacity: 0.75;
    transition: all 0.5s;

    &.selected {
      opacity: 1;
    }

    &:hover {
      opacity: 0.3;
    }

    &:first-child {
      margin-left: 0;
    }


  }

  &__link-icon {
    width: 16px;
    height: 16px;
    margin-right: 8px;
  }
}
</style>
