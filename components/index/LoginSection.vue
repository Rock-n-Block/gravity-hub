<template lang="pug">
  section.login-section(v-if="openLogin")
    div.container(v-if="!openRegistration")
      div.close-section(v-on:click="close()")
        span.close-section-item
        span.close-section-item
      div.login-block
        span.login-block-title Connect to get started
        div.login-block-buttons
          span.button.button-waves-signer Waves Signer
          span.button.button-waves-keeper(v-on:click="openRegistration = !openRegistration") Waves Keeper
    <registration-section @close-registration="openRegistration = !openRegistration" v-bind:open-registration="openRegistration" />
</template>

<script>
import RegistrationSection from "./RegistrationSection.vue";

export default {
  props: ["openLogin"],
  data: function() {
    return {
      openRegistration: false
    };
  },
  components: {
    RegistrationSection
  },
  methods: {
    close() {
      this.$emit("close-login");
    }
  }
};
</script>

<style lang="scss" scope>
@import "../../assets/scss/mixins/media";

.close-section {
  @include bb(endmobile, 0) {
    top: 25px;
    right: 15px;
  }
}

.login-block {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;

  &-title {
    text-align: center;
    display: block;
    margin-bottom: 50px;
    font-size: 24px;
    color: white;
    font-weight: bold;

    @include bb(endmobile, 0) {
      font-size: 20px;
      margin-bottom: 20px;
    }
  }

  &-buttons {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    width: 100%;
  }

  .button {
    margin-bottom: 20px;
    color: white;
    width: 100%;
    max-width: 450px;
    text-align: center;
    padding: 20px 10px;
    font-size: 16px;

    &:hover {
      opacity: 0.6;
    }
  }
}

.login-section {
  z-index: 99;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 10px;
  align-items: center;
  display: flex;
  justify-content: center;
  background-color: #353540fc;

  .container {
    max-width: 1150px;
    background-color: #2d3044;
    padding: 50px 100px;
    position: relative;
    width: 100%;

    @include bb(tablet, 0) {
      padding: 40px 20px;
    }

    @include b(mobile) {
      padding: 20px 20px;
    }

    @include bb(endmobile, 0) {
      padding: 40px 20px;
    }
  }
}
</style>
