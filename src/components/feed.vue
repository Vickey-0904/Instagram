<template>
<div class="feed">
  
  <div class="post">

      <div class="title">      
        <div><img :src="posts.dp" alt="" class="p-pic"></div>
        <div class="name">{{posts.Name}} <br> <span style="font-size: 12px; font-weight: 200; color: #8D98A1 ">{{posts.Location}}</span> </div>
        <div class="dots">
          <div class="d"></div>
          <div class="d"></div>
          <div class="d"></div>
        </div>
      </div>
      <div class="image">
        <img :src="posts.post" class="i" alt="">
      </div>
      <div class="foot">
        <div class="like"> <img src="../assets/like.svg" width="20px" alt="">
        <span style="font-family: 'Roboto', sans-serif; font-size: 14px;font-weight: bold; margin-left: 5px; color: #1A1C27">{{posts.like}}</span>
        </div>
        <div class="cmt"> <img src="../assets/cmt.svg" width="20px" alt="">
        <span style="font-family: 'Roboto', sans-serif; font-size: 14px; font-weight: bold; margin-left: 5px; color: #1A1C27">{{posts.cmt}}</span>
        </div>
        <div class="send">
          <img src="../assets/share.svg" width="20px" alt="">
        </div>
        <div class="save">
          <img src="../assets/save.svg" width="20px" alt="">
        </div>
      </div>
      <div class="others">
        <div style="display:flex; align-items: center;"> 
        <img src="../assets/post/dp/a.jpg" alt="" class="o-pic">
        <img src="../assets/post/dp/c.png" alt="" class="o-pic">
        <img src="../assets/post/dp/e.jpg" alt="" class="o-pic">
        </div>
        <div class="o-text">
          James, Dia, Lisa, Kate, Ben, Leo...
        </div>
        <div class="more">
          More
        </div>
       
      </div>
  </div>
</div>


</template>

<script>
// import bubbles from './bubbles.vue';
export default {
  props: ['posts'],
  components: { 

   },
  name: 'App',
      data () {
        return {
          ninjas: [
               {
                picture: require("../assets/a.png"), name: 'a', location: 'a', likes: 'a', comments: 'a',
            },
                           {
                picture: require("../assets/a.png"),name: 'b', location: 'b', likes: 'b', comments: 'b',
            },
                           {
                picture: require("../assets/a.png"),name: 'c', location: 'c', likes: 'c', comments: 'c',
            },
              {
                picture: require("../assets/a.png"),name: 'd', location: 'd', likes: 'd', comments: 'd',
            },
              {
                picture: require("../assets/a.png"),name: 'e', location: 'e', likes: 'e', comments: 'e',
            },
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
      .feed{
        display: flex;
        justify-content: center;
        margin-bottom: 20px;
      }
.post{
  width: 340px;
  height: 485px;
  overflow: hidden;
  background-color: #FEFEFE;
  border-radius: 25px;
  z-index: 1;
}
.d{
  width: 4px;
  height: 4px;
  background-color: #1A1C27;
  border-radius: 100px;
  margin-left: 2px;
}
.dots{
  display: flex;
  margin-right: 20px;
  align-items: center;
}
.p-pic{
  width: 35px;
 // height: 30px;
  border-radius: 100px;
  margin-left: 10px;
}
.title{
  display:flex;
  justify-content: space-between;
  margin-top: 10px;
}
.name{
  font-size: 14px;
        font-family: 'Roboto', sans-serif;
        font-weight: bold;
        flex: 1;
        margin-left:10px ;
        color: #1A1C27 ;
}
.i{
  
  border-radius: 25px;
  overflow: hidden;
  width: 320px;
  margin-top: 10px;
}
.image{
display: flex;
  justify-content: center;
  margin-bottom: 10px;
}
.image::before{
content: "";
position: absolute;
width: 250px; height: 250px;
background-image: url("../assets/post/d2.png");
background-size: cover;
z-index: -1;
display: block;
margin: 80px auto 0px auto;
//top: 34%; 
//left: 15%;
filter: blur(20px);
display: flex;
justify-content: center;
align-items: center;
}
.like{
  width: 80px;
  height: 44px;
  background-color: #EAEEF1;
 z-index: -2;
  border-radius: 18px;
  margin-left: 10px;
  display:flex;
  justify-content: center;
  align-items: center;
  //opacity: 50%;
  position: relative;
}

.cmt{
   margin-left: 20px;
   align-items: center;
   display: flex;
   
}
.send{
   margin-left: 20px;
   align-items: center;
   display: flex;
   transform: rotate(-35deg);
   
}
.save{
 // margin-left: 20px;
   align-items: center;
   display: flex;
   flex: 1;
   justify-content: flex-end;
   margin-right: 25px;
}
.foot{
  display: flex;
  
}
.o-pic{
   width: 20px;
  height: 20px;
  border-radius: 100px;
  margin-left: 10px;
  border: 2px solid white;
  //display:flex;
  //justify-content: center;
  align-items: center;
  position: absolute;
  max-width: 100%;
}
.o-pic:nth-child(1) {
  position: absolute;
  left: 15px;
  z-index: -1;
}
.o-pic:nth-child(2) {
  position: absolute;
  left: 28px;
  z-index: -2;
}
.others{
  display: flex;
  justify-content: space-around;
  position: relative;
  margin-top: 10px;
}
.o-text{
   font-size: 12px;
        font-family: 'Roboto', sans-serif;
        color: #1A1C27 ;
        display:flex;
  justify-content: center;
  align-items: center;
  margin-left: 55px;
 flex: 1;
}
.more{
   font-size: 12px;
        font-family: 'Roboto', sans-serif;
        font-weight: bold;
        color: #1A1C27 ;
          width: 70px;
  height: 30px;
  background-color: #EAEEF1;
   border-radius: 18px;
 // margin-left: 10px;
  display:flex;
  justify-content: center;
  align-items: center;
  margin-right: 10px;
}
    }
</style>
