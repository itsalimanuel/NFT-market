<template>
  <header class="header">
    <nav class="header-nav">
      <div class="header-logo">
        <img alt="" :src="require('@/assets/logo.svg')" />
      </div>
      <div class="header-links">
        <router-link to="/">Auctions</router-link>
        <router-link to="/">Roadmap</router-link>
        <router-link to="/">Discover</router-link>
        <router-link to="/">Community</router-link>
      </div>
      <div class="header-actions action">
        <a class="action-contact" href=""> Contact </a>
        <a class="action-account" href=""> My account </a>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "nav-components"
};
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  padding: 36px;

  &-nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &-logo {
    width: 170px;
    height: 30px;

    img {
      width: 100%;
      height: 100%;
    }
  }

  &-links {
    a {
      margin-right: 15px;
      letter-spacing: 0.2px;
      font-size: 14px;
      font-weight: 500;
      text-decoration: none;
      color: #7780a1;

      &:last-child {
        margin-right: 0;
      }
    }
  }

  &-actions {
    .action-account {
      background: linear-gradient(104.42deg, #4745d0 0%, #2a27c9 60.23%);
      box-shadow: inset -4px -4px 4px rgba(0, 0, 0, 0.1),
        inset 4px 4px 4px rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      padding: 10px 16px;
      color: #ffffff;
    }

    .action-contact {
      border: 2px solid #7780a1;
      //box-shadow: inset -4px -4px 4px rgba(0, 0, 0, 0.1), inset 4px 4px 4px rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      padding: 10px 16px;
      color: #7780a1;
    }

    a {
      margin-right: 15px;
      letter-spacing: 0.2px;
      font-size: 14px;
      font-weight: 500;
      text-decoration: none;

      &:last-child {
        margin-right: 0;
      }
    }
  }
}
</style>
