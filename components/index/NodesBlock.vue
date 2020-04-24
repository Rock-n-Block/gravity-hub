<template lang="pug">
  section.block.block-nodes
    div.container-content
      div.block-text
        div.block-text-wrap
          h2.text.text-title Nodes
          p.text
            b Gravity Hub’s nodes
            |  will be able, for instance, to obtain block headers from the Ethereum network and send them to Waves Platform.
          p.text If Ethereum block header data is available on Waves Platform, it will be possible to prove that a specific transaction has taken place on Ethereum.  To obtain that data, users will pay reasonable fees.
          p.text
            b Gravity Hub
            |  will also be connected to custom chains, which represent a new approach to blockchain customization. Waves Matter, our blockchain engine, can be assembled in any configuration for different purposes.
      div.block-image
        img.block-image-wrap(src='img/nodes-3.png',alt='nodes')
</template>

<style lang="scss" scoped>
@import "../../assets/scss/mixins/media.scss";
@import "../../assets/scss/mixins/image.scss";

.block {
  &-nodes {
    position: relative;

    @include before-img(block, 250px, 250px, a) {
      background-image: url("~static/img/rm_01.png");
      background-size: 100%;
      background-repeat: no-repeat;
      top: -120px;
      left: 150px;
      z-index: 1;

      @include b(1440) {
        top: -120px;
        left: -130px;
      }
    }

    .container-content {
      max-width: 1370px;
      grid-gap: 0;
      grid-template-columns: minmax(300px, 600px) minmax(300px, 750px);

      @include b(mobile) {
        display: flex !important;
        flex-direction: column;
        padding: 0 20px;
      }

      .block {
        &-text {
          background: url("~static/img/bg-title-node.png") no-repeat center -10px/90%;
          padding-right: 70px;
          display: flex;
          justify-content: flex-end;

          @include bb(tablet, 0) {
            background: url("~static/img/bg-title-node.png") no-repeat left
              top/90%;
            padding-right: 20px;
          }

          @include b(mobile) {
            background: url("~static/img/bg-title-node.png") no-repeat left
              top/contain;
            padding-right: 0px;
          }

          &-wrap {
            width: 100%;
            max-width: 370px;

            @include b(mobile) {
              max-width: 100%;
            }
          }

          .text {
            opacity: 0.75;

            &-title {
              opacity: 0.8;
            }
          }
        }
      }
    }
  }
}
</style>
