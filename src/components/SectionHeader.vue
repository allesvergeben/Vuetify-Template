<template>
  <div class="section-header text-center mb-12 mt-5">
    <h2
      class="text-uppercase caption mb-4"
      v-text="header"
    />
    <v-divider class="mt-5 mb-4 mx-auto" />
    <h3
      class="display-1 font-weight-light"
      v-text="subHeader"
    />
  </div>
</template>

<script>
  export default {
    props: {
      header: {
        type: String,
        default: ''
      },
      subHeader: {
        type: String,
        default: ''
      }
    }
  }
</script>

<style lang="stylus">
  .section-header
    .v-divider
      border-width: 1px
      width: 150px
</style>
