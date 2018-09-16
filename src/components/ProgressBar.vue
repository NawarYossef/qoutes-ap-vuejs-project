<template>
  <div>
    <div class="col-xs-12 container">
      <header>
        <h2>Qoutes Added</h2>
        <div class="progress progress-bar progress-bar-striped progress-bar-animated active" role="progressbar" aria-valuenow="70" aria-valuemin="0" aria-valuemax="100" :style="{width:progress}">
          {{progress}}
        </div>
      </header>
    </div>
  </div>
</template>

<script>
// import {eventBus} from "../main";

export default {
  props: {
    progress: String
  }
};
</script>

<style lang="scss" scoped>
.container {
  padding: 0px {
  }
  header {
    margin: 40px auto 0 auto;
  }
}
</style>
