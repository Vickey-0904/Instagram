<template>
  <div class="bubbles">

<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>

  </div>
  
</template>

<script>
export default {
  name: 'bubbles',

  data () {
        return {
          ninjas: [
              {name: 'Ryu'},
              {name: 'Crystal'},
              {name: 'Hitoshi'},
              {name: 'Tango'},
              {name: 'Kami'},
              {name: 'Yoshi'}
          ],
}
console.log("Hello");
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header-style{
    @media (max-width: 576px) { 
display: flex;
overflow-x: auto;
padding:5px 0 5px 0;
     }
    .noti{
      position: absolute;
      width: 8px;
      height: 8px;
      background-color: #FC045C;
      color: red;
      border-radius: 50px;
      right: 12px;
      top: 27px;
    }

    .st{
    //    width: 100px;
     // height: 100px;
     // background-color: #FC045C;
      border-radius: 50px;
    
    }
body::-webkit-scrollbar {    display: none;}
}
</style>
