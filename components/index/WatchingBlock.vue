<template lang="pug">
  section.block.block-watching
    div.container-content
      div.block-image
        img.block-image-wrap(src='img/watching_data-3.png', alt='watching data').
        div.block-image-text
          div.block-image-text-wrap
            p.text All Gravity Hub nodes will have “data watchers” — modules for collecting various types of data, such as block headers and block height from other blockchains, exchange rates, etc.
            p.text For each data watcher, a data profile will be set. For a, if a data watcher collects Ethereum block header data, this will need to be done with a certain frequency and reliability.
      div.block-text
        h2.text.text-title
          | Watching
          |
          | data
        p.text In addition to providing an interoperability protocol, Gravity Hub will help resolve the issue of obtaining information from the outside world, as it will facilitate access of all connected chains to data from outside the blockchain.
        p.text A member of any network connected to Gravity Hub will be able to request oracle data from any information systems that have APIs — from Google to enterprise ERP systems.
</template>

<style lang="scss" scoped>
@import "../../assets/scss/mixins/media.scss";

.block {
  &-watching {
    background-image: url("~static/img/rm_02.png") no-repeat right 60px/200px;

    @include b(1024) {
      background: none;
    }

    .container-content {
      grid-template-columns: minmax(300px, 850px) minmax(300px, 390px);
      max-width: 1310px;

      @include b(mobile) {
        display: flex !important;
        flex-direction: column-reverse;
        padding: 0 20px;
      }

      .block {
        &-image {
          z-index: 1;

          &-text {
            margin-top: -80px;
            display: flex;
            justify-content: center;
            width: 100%;

            &-wrap {
              width: 100%;
              max-width: 580px;
            }
          }
        }

        &-text {
          background: url("~static/img/bg-title-watching.png") no-repeat -20px -20px/100%
            50%;
          padding-right: 10px;
        }
      }
    }
  }
}
</style>
