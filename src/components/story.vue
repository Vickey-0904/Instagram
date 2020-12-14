<template>
  <div class="header-style ">
<!-- <div><img src="../assets/add(1).svg" alt="">d</div> -->
<div style="margin-right: 8px; font-size: 12px; margin-left: 1.5rem" ><div><img src="../assets/add(1).svg" alt="" width="17rem" class="add"></div><div style="font-family: 'Roboto', sans-serif; font-weight: bold;">Your story </div></div>


      <div v-for='ninja in ninjas' :key='ninja._id' > 
          <img v-bind:src="ninja.picture" v-bind:alt="fdf" class="st-pic">
          <span class="na">{{ninja.name}}</span>
          </div>
<!-- <div v-for='ninja in ninjas'
    :key='ninja._id' > {{ninja.name}}</div> -->
<!-- <div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div>
<div class="st"><img src="../assets/logo.png" alt=""></div> -->
  <bubbles/>
  </div>

</template>

<script>
// import bubbles from './bubbles.vue';
export default {
  components: {  },
  name: 'App',
      data () {
        return {
          ninjas: [
               {
                picture: require("../assets/story/s3.png"), name: 'William',
            },
                           {
                picture: require("../assets/story/s4.jpg"),name: 'Jessy',
            },
                           {
                picture: require("../assets/post/dp/e.jpg"),name: 'James',
            },
              {
                picture: require("../assets/a.png"),name: 'Lisa',
            },
              {
                picture: require("../assets/post/dp/d.jpg"),name: 'Ben',
            },
              {
                picture: require("../assets/post/dp/a.jpg"),name: 'Dia',
            },
              {
                picture: require("../assets/post/dp/b.png"),name: 'Noah',
            }
            
          ],
          title: 'Vue Wizards'
        }
    }

}
console.log("Hello");
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

    @media (max-width: 576px) { 
        .header-style{
          
display: flex;
overflow-x: scroll ;
//overflow-x: auto;
//padding:5px 0 5px 0;
text-align: center;
//justify-content: center;
align-items: center;
border-top:solid rgba(176, 186, 191, 0.43) 1px;
border-bottom:solid rgba(176, 186, 191, 0.43) 1px;
padding-top: 6px;
padding-bottom: 3px;
margin-bottom: 20px;
//margin-left: 1.5rem; margin-right:1.5rem;
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

    .st-pic{
    //    width: 100px;
     // height: 100px;
     // background-color: #FC045C;
     // border-radius: 100px;
    //margin-right: 20px;
    width: 3.5rem;
    display: block;
  //margin-left: 2px;
   margin-right: 8px;
  border: double 3px transparent;
  border-radius: 100px;
  background-image: linear-gradient(#e1306c, #c13584), radial-gradient(circle at top left, #405de6,#5851db,#833ab4,#c13584,#e1306c,#fd1d1d);
  background-origin: border-box;
  background-clip: content-box, border-box;
//   border-image-source: linear-gradient(45deg, rgb(0,143,104), rgb(250,224,66));
//   border-image-slice: 1;
//   border-radius: 100px;
    }

    .na{
        // margin: 29%;
        font-size: 12px;
        font-family: 'Roboto', sans-serif;
        font-weight: bold;
    }
.header-style::-webkit-scrollbar {    display: none;}
}

.add{
    display: block;
   // justify-content: center;
    //align-items: center;
    background-color: #E9EBED;
    padding: 21px;
    border-radius: 100px;
    border:2px solid #D2D6DA;
    margin-top: 0;
    //max-width: 3.5rem;

}
.circle{
    width: 100px;
    height: 100px;
    background-color: red;
}
</style>
