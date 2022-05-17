<template>
  <header class="header">
    <div class="header__logo">
      <img src="../assets/img/la-molisana-logo.png" alt="" />
    </div>
    <nav>
      <ul class="header__menu">
        <li
          v-for="(item, index) in links"
          :key="index"
          :class="{ active: item.active }"
        >
          <a href="">{{ item.text }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  data: function () {
    return {
      links: [
        {
          url: "#",
          text: "Home",
          active: false,
        },
        {
          url: "#",
          text: "Prodotti",
          active: true,
        },
        {
          url: "#",
          text: "Chi siamo",
          active: false,
        },
        {
          url: "#",
          text: "Contatti",
          active: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

//.header__logo

.header {
  &__logo {
    text-align: center;

    img {
      min-width: 300px;
    }
  }

  &__menu {
    display: flex;
    justify-content: center;

    li {
      margin: 0.5rem;
      padding: 0.5rem;

      &.active {
        background-color: $brand-secondary-color;
      }

      a {
        color: $text-color;
      }
    }
  }
}
</style>