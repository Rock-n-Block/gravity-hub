<template lang="pug">
  section.section-gravity-hub
    div.container-content
      div.block-gravity-hub
        h2.text.text-title Join Gravity Hub
        p.text To become a Gravity Hub member, a user will need to install a Gravity Hub node and, for that purpose, to lock a certain sum of money on any of the supported public blockchain networks.
        p.text You can lock a certain sum on the Ethereum network for a fixed period, using a special smart contract. Once you’ve done that, you’ll be able to collect revenues from users’ data requests, also enjoying Gravity Hub’s other advantages.
        span.button.button-orange Install GH node
        div.img-block
          img(src='img/cos.png', alt='cosmonaut')
          img(src='img/mob_space.png', alt='cosmonaut')
</template>

<style lang="scss" scoped>
@import "../../assets/scss/mixins/media.scss";

section.section-gravity-hub {
  display: flex;
  justify-content: center;
  margin-top: -150px;
  z-index: 1;

  @include b(1024) {
    background: none;
  }

  @include b(mobile) {
    margin-top: 0;
  }

  .container-content {
    max-width: 1200px;
    width: 100%;
    height: 1200px;
    justify-content: center;
    align-items: center;
    display: flex;
    z-index: 1;
    background: url("~static/img/space.png") no-repeat center / 100%;

    @include bb(tablet, 0) {
      height: 1020px;
    }

    @include b(mobile) {
      padding: 20px;
      height: auto;
      background: none;
    }

    @include b(mobile) {
      margin-bottom: 15px;
      font-size: 14px;
      line-height: 20px;
    }

    .block-gravity-hub {
      width: 100%;
      max-width: 555px;
      z-index: 1;

      @include bb(tablet, 0) {
        max-width: 325px;
      }

      @include b(mobile) {
        max-width: 100%;
      }

      .text {
        margin-bottom: 20px;
        font-size: 17px;
        line-height: 28px;
        opacity: 0.74;
        padding: 0 35px;

        @include b(tablet) {
          margin-bottom: 15px;
          font-size: 14px;
          line-height: 20px;
          padding: 0;
        }

        &-title {
          text-align: center;
          width: 100%;
          font-size: 48px;
          line-height: 50px;
          margin-bottom: 40px;
          opacity: 0.8 !important;

          @include bb(tablet, 0) {
            font-size: 30px;
            line-height: 20px;
            margin-bottom: 30px;
          }

          @include b(mobile) {
            font-size: 25px;
            line-height: 20px;
            margin-bottom: 30px;
          }
        }
      }

      .button {
        text-align: center;
        width: 100%;
        max-width: 270px;
        height: 50px;
        margin: 0 auto;
        color: white;
        margin-top: 30px;
        z-index: 1;
        position: absolute;
        left: 0;
        right: 0;

        @include b(tablet) {
          max-width: 160px;
          margin-top: 10px;
          font-size: 14px;
        }

        @include b(mobile) {
          max-width: 240px;
          margin-top: 10px;
        }
      }

      .img-block {
        width: 100%;
        z-index: 0;
        display: block;
        margin-top: 30px;
        text-align: center;

        @include b(500) {
          text-align: center;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-top: 20px;
        }

        img {
          &:nth-child(1) {
            @include b(500) {
              display: none;
              max-width: 450px;
            }
          }

          &:nth-child(2) {
            display: none;

            @include b(500) {
              display: block;
              max-width: 320px;
            }
          }
        }
      }
    }
  }
}
</style>
