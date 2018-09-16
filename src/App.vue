

<template>
  <div class="container">
    <ProgressBar :progress="progress"></ProgressBar>
    <hr>
    <AddQouteForm v-model="qoute" :handleSubmit="handleSubmit"></AddQouteForm>
    <Qoutes :qoutes="qoutesArr" :deleteQoute="deleteQoute"></Qoutes>
    <AppInfo></AppInfo>
  </div>
</template>

<script>
import ProgressBar from "./components/ProgressBar.vue";
import AddQouteForm from "./components/AddQouteForm.vue";
import Qoutes from "./components/Qoutes.vue";
import AppInfo from "./components/AppInfo.vue";

export default {
  data() {
    return {
      qoutesArr: [],
      progress: null,
      qoute: "",
      maxQoutes: 10,
      formIsSubmitted: false
    };
  },
  methods: {
    handleSubmit() {
      if (this.qoute) {
        this.qoutesArr.push(this.qoute);
        this.updatePorgress();
      } else {
        alert("Please write a qoute. Empty qoutes are not allowed");
      }
    },
    deleteQoute(idx) {
      this.qoutesArr.splice(idx, 1);
      this.updatePorgress();
    },
    updatePorgress() {
      this.progress = `${this.qoutesArr.length * 10}%`;
    }
  },
  components: {
    ProgressBar,
    AddQouteForm,
    Qoutes,
    AppInfo
  }
};
</script>

<style lang="scss" scoped>
.container {
  max-width: 1350px;
}
</style>





