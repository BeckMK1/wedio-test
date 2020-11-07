<template>
    <div class="modal" v-if="!isHidden">
        <header>
            <img src="../assets/images/logo-wedio-white.svg" alt="wedio logo">
            <p>The only true opinion </p>
        </header>
        <section>
            <p>Dota 2 is better than LoL in every conceivable way possible</p>
            
        </section>
        <footer>
            <div class="modal-cta">
                <button class="wedio-button tiny" @click="Iagree = !Iagree, isHidden = !isHidden, isFocus = !isFocus, fade()">I agree</button>
                <button class="wedio-button tiny" @click="isHidden = !isHidden, isFocus = !isFocus ">I don't agree</button>
            </div>
        </footer>
    </div>
    <div class="modal-focus" v-show="!isFocus" @click="isHidden = !isHidden, isFocus = !isFocus"></div>
    <button class="wedio-button" @click="isHidden = !isHidden,  isFocus = !isFocus">Call To Action</button>
    <div class="agree" v-show="Iagree">&#10003;</div>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return{
      isHidden: true,
      isFocus: true,
      Iagree: false
    }

  },
  methods:{
  fade(){
    setTimeout(() => this.Iagree = false, 1000)
    },
    }
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables.scss';
@import '../assets/styles/buttons.scss';
.modal{
    width: 500px;
    background: $white;
    left: calc(50% - 250px);
    bottom: 70%;
    position: absolute;
    z-index: 3;
header{
    background: $black;
    color: $white;
    padding-top: 16px;
    padding-bottom: 4px;
    img{
        height: 14px;
    }
    p{
        margin-top: 4px;
    }
}
footer{
    background: $black;
        padding-top: 16px;
    p{
        margin: 0;
    }
}
}
.modal-cta{
display: flex;
justify-content: center;
justify-content: space-around;
}
.modal-cta  :nth-child(1){
   background: green;

}
.modal-cta :nth-child(2){
    background: red;
}
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
.wedio-button{
    margin-bottom: 18px;
}
.agree{
width: 150px;
height: 150px;
background: green;
border-radius: 100%;
color: white;
display: flex;
align-items: center;
justify-content: center;
font-size: 5rem;
position: absolute;
left: calc(50% - 75px);
bottom: 70%;
z-index: 5;
animation: start 1s;
opacity: 0;
}
@keyframes start {
    from{
        transform: scale(0);
        opacity: 1;
    }
    to {
        transform: scale(1.0);
        opacity: 0;
    }
}

</style>