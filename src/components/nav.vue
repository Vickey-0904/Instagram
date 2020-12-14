<template>
  <div class="nav">
<img src="../assets/home.svg" width="20px" alt="">
<img src="../assets/search.svg" width="20px" alt="">
<img src="../assets/p-add.svg" width="20px" alt="">
<div style="position: relative"><img src="../assets/heart.svg" width="20px" alt="" style="position: relative"> <span class="s"></span></div>



<img src="../assets/user.svg" width="20px" alt="">
  </div>
</template>

<script>
export default {
     components: {  },
  name: "Nav",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @media (max-width: 576px) {
  .nav{
      display: flex;
      justify-content: space-around;
      position:fixed;
      bottom: 0;
      width:100%;
      padding: 12px 0px;
      border-top-left-radius: 20px;
      border-top-right-radius: 20px;
//height: 30px;
background-color: #ffffff;
z-index: 4;

// -webkit-box-shadow: -1px 0px 5px 0px rgba(50, 50, 50, 0.75);
// -moz-box-shadow:    -1px 0px 5px 0px rgba(50, 50, 50, 0.75);
// box-shadow:         -1px 0px 5px 0px rgba(50, 50, 50, 0.75);
  }

  .s{
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #fc045c;
    border-radius: 50px;
    right: -3px;
    top: 0px;
   // z-index: 9;
   display: block;
  // 	background: #f49d16;
	cursor: pointer;
	//box-shadow: 0 0 0 rgb(244,157,22);
	animation: pulse 2s infinite;
  }

//   @-webkit-keyframes pulse {
//   0% {
//     -webkit-box-shadow: 0 0 0 0 rgba(244,157,22, 0.4);
//   }
//   70% {
//       -webkit-box-shadow: 0 0 0 10px rgba(244,157,22, 0);
//   }
//   100% {
//       -webkit-box-shadow: 0 0 0 0 rgba(244,157,22, 0);
//   }
// }
@keyframes pulse {
  0% {
    -moz-box-shadow: 0 0 0 0 rgba(253,33,110, 0.4);
    box-shadow: 0 0 0 0 rgba(253,33,110, 0.4);
  }
  70% {
      -moz-box-shadow: 0 0 0 10px rgba(253,93,149, 0);
      box-shadow: 0 0 0 10px rgba(253,93,149, 0);
  }
  100% {
      -moz-box-shadow: 0 0 0 0 rgba(253,174,202, 0);
      box-shadow: 0 0 0 0 rgba(253,174,202, 0);
  }
}
}
</style>
