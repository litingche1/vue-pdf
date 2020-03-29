<template>
  <div class="hello">
    <div style="margin-top: 30px;color: #70DB55">
      <span style="font-weight: 600" @click="checkContract">点我试试</span>
    </div>
    <vuepdf :visible="contractVisable" :showBtns="true" @handleModal="close"></vuepdf>
  </div>
</template>

<script>
import vuepdf from "./pdf.vue";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  components: {
    vuepdf
  },
  data() {
    return {
      showPdf: false,
      contractVisable: false
    };
  },
  methods: {
    checkContract() {
      this.contractVisable = !this.contractVisable;
    },
    close() {
      this.contractVisable = false;
    }
  }
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
