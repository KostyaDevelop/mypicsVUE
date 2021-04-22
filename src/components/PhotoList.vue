<template>
  <div class="head_page">
    <div class="row">
      <div class="col-lg-4 col-md-4 col-sm-4">
      {{info}}wwwwwwwww
        <div class="avatar-box">
                           <a href="">
          <img class="avatar" src="">
                         </a>
        </div>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4">
        <div class="row-1 info-user">
          <span class="head_page_item head_page_item_login"></span>
        </div>
        <div class="row-2 info-user">
                    <span class="head_page_item head_page_item-count">
                            <b  class="head_page_item_count-number">0</b>
                            публикаций
                    </span>
          <span class="head_page_item head_page_item-count">
                        <b  class="head_page_item_count-number">-</b>
                        подпичсчиков
                    </span>
          <span class="head_page_item head_page_item-count">
                        <b  class="head_page_item_count-number">-</b>
                        подпичсок
                    </span>
        </div>
        <div class="row-3 info-user">
          <b class="head_page_item head_page_item-name">
          </b>
        </div>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PhotoLIst",
  props: {
    albumPage: {
      required: true,
      type: [Object, Array]
    },
    albumFiles: {
      required: true,
      types: [Array, Object]
    },
    pageData: {
      required: true,
      types: [Array, Object]
    },
    editAccess: {
      type: Boolean,
      default: false
    }
  },
  data: function () {
    return {
      count: 0
    }
  },
  mounted () {
    this.axios
      .get('http://mypics.localhost/getapi')
      .then(response => (this.info = response))
  }
}
</script>

<style scoped>

</style>
