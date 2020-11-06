<template>
    <div class="modal">
        <header>
            <img src="../assets/images/logo-wedio-white.svg" alt="wedio logo">
            <p>this is a header</p>
        </header>
        <section>
            <p>content</p>
        </section>
        <footer>
            <p>this is a footer</p>
        </footer>
    </div>
</template>
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
    color: $white;
    p{
        margin: 0;
    }
}
}
</style>