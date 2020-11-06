<template> 
<div class="modal-button">
    <div class="modal-content" v-show="!isHidden">
      <Modal></Modal>
    </div>
    <div class="modal-focus" v-show="!isFocus" @click="isHidden = !isHidden, isFocus = !isFocus"></div>
    <button class="wedio-button" v-on:click="isHidden = !isHidden,  isFocus = !isFocus">Call To Action</button>
    </div>
</template>
<script>
// @ is an alias to /src
import Modal from "@/components/Modal.vue";

export default {
  name: "Home",
  components: {
    Modal
  },
  data() {
    return{
      isHidden: true,
      isFocus: true
    }
  }
};
</script>
<style lang="scss" scoped>
@import '../assets/styles/buttons.scss';
.modal-focus{
  background: black;
position: absolute;
top:0;
bottom:0;
left: 0;
right: 0;
z-index: 2;
opacity: 70%;
}
</style>