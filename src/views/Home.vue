<template>
  <div class="home">
    <h1>This is home page</h1>
    <img alt="Vue logo" src="../assets/images/logo-wedio-black.svg" class="wedio-logo"/>
    <Content msg="Welcome to Your Wedio Internship Test" />
    <Modal></Modal>
  </div>
</template>

<script>
// @ is an alias to /src
import Content from "@/components/Content.vue";
import Modal from "@/components/Modal.vue";

export default {
  name: "Home",
  components: {
    Content,
    Modal
  }
};
</script>

<style lang="scss" scoped>
.home{
  margin-top: 80px;
}
.wedio-logo{
  max-width: 800px;
  max-height: 400px;
}
h1{
  margin-top: 100px ;
}

</style>
