<template lang="pug">
  section.block.block-reaching
    div.container-content
      div.container-content-wrap
        div.block-text
          h2.text.text-title
            | Reaching
            |
            | consensus
          p.text How can we make sure that data provided by Gravity Hub is accurate? That can be achieved by consensus between several nodes.
          p.text One option is a multi-signature solution, whereby a transaction containing the consensus data must be signed by all nodes.
        div.block-image
          img.block-image-wrap(src='img/reaching_consensus-2.png', alt='watching data')
          div.block-image-text
            div.block-image-text-wrap
              p.text Alternatively, any node could be allowed to send consensus data to the user, but in that case, the node’s stake will act as collateral. If, for instance, a node sends data to the target blockchain that is different from the ultimate consensus data, proof of that can be sent to a smart contract, which will automatically deduct part of the node’s stake as a fine.
              p.text A user will be able to request a certain type of data over a specific time period for a fee consisting of execution costs and the node’s fee. Also, the user will be able to set up preferences. For example, when requesting exchange rate data, the user can set the maximum variability required.

</template>

<style lang="scss" scoped>
@import "../../assets/scss/mixins/media.scss";

.block {
  &-reaching {
    background: url("~static/img/rm_03.png") no-repeat left center/contain;

    @include b(1024) {
      background: none;
    }

    .container-content {
      max-width: 1450px;
      // display: flex !important;
      justify-content: flex-end !important;

      @include b(mobile) {
        padding: 0 20px;
      }

      &-wrap {
        grid-template-columns: minmax(300px, 390px) minmax(300px, 850px);
        max-width: 1240px;
        width: 100%;
        display: grid;
        z-index: 2;

        @include b(mobile) {
          display: flex !important;
          flex-direction: column;
        }
      }

      .block {
        z-index: 1;

        &-image {
          &-text {
            margin-top: -100px;
            display: flex;
            justify-content: center;

            &-wrap {
              width: 100%;
              max-width: 580px;
            }
          }
        }

        &-text {
          background: url("~static/img/bg-title-reaching.png") no-repeat center -40px/100%;
        }
      }
    }
  }
}
</style>
