<template>
  <nuxt />
</template>

<style lang="scss">
@import "../assets/scss/mixins/media.scss";
@import "../assets/scss/mixins/image.scss";

:root {
  --bg-color: #353540;
  --overlay-color: linear-gradient(
    180deg,
    rgba(24, 27, 44, 0.95) -5.12%,
    #0d0f14 102.43%
  );
  --text-color: #ffffff;
  --title-color: #fafafa;
  --bold-color: #fafafa;
  --accent-color: #ff8e1e;
  --like-color: #ff0000;
  --color-orange: #ff8e1e;
  --color-orange-accent: #e17f1d;

  // --container-width: 1200px;
  --container-width: 1250px;
  --container-content-width: 1100px;
  --container-paddings-desctop: 10px 50px;
  --container-paddings-tablet: 10px 40px;
  --container-paddings-mobile: 10px 10px;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}

html {
  box-sizing: border-box;
}

.overlay {
  position: relative;

  &-bg {
    position: absolute;
    top: 0;
    z-index: -1;
    left: 0;
    width: 100%;
    background: var(--overlay-color);
    height: 100%;
    display: block;
    // backdrop-filter: blur(122.323px);
  }
}

body {
  margin: 0;
  background-color: var(--bg-color);
  // backdrop-filter: blur(122.323px);
  font-family: "Poppins", sans-serif;
  cursor: default;
}

.container {
  max-width: var(--container-width);
  padding: var(--container-paddings-desctop);
  margin: 0 auto;

  @include b(1024) {
    padding: var(--container-paddings-tablet);
  }

  @include b(750) {
    padding: var(--container-paddings-mobile);
  }
}

.container-content {
  max-width: var(--container-content-width);
  padding: var(--container-paddings);
  margin: 0 auto;
  padding: 0 40px;
}

p {
  padding: 0;
  margin: 0;
  line-height: 1;
  color: var(--text-color);
  font-weight: normal;
}

b {
  color: var(--bold-color);
}

.text {
  display: inline-block;
  font-weight: 300;

  &-accent {
    color: var(--accent-color);
  }

  &-title {
    color: var(--title-color);
    font-weight: bold;
    font-family: Orbitron;
    letter-spacing: 2px;
  }
}

.icon-like {
  color: red;
  font-size: 17px;
}

.button {
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;

  &-orange {
    background-color: var(--color-orange);

    &:hover {
      background-color: var(--color-orange-accent);
    }
  }

  &-login {
    color: var(--text-color);
    font-size: 16px;
    font-weight: 500;

    &:hover {
      color: var(--color-orange-accent);
    }

    @include before-img(block, 18px, 18px, r) {
      background-image: url("~static/img/icons/login.svg");
      background-size: cover;
      margin-right: 10px;
    }
  }
}

.logo {
  background-image: url("~static/img/logo.svg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  width: 133px;
  height: 60px;

  @include b(550) {
    width: 130px;
    height: 55px;
  }
}

img {
  max-width: 100%;
}

a {
  text-decoration: none;
}

a,
p,
.button,
span {
  transition: 0.4s ease;
}
</style>