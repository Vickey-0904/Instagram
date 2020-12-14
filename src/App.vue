<template>
  <div id="app">
<Header class="dis"/>
<story class="dis"/>
<feed  
v-for="posts in feed"
:key="posts.color"
:posts="posts"
 class="dis"/>
<!-- <feed />
<feed />
<feed />
<feed /> -->
<Nav class="dis"></Nav>
<div class="alert">
 <span class="n">Note</span>  <br>
  <span class="txt">The Instagram app is designed only for mobile resolution (i.e. below 414px). Please view using browser development tools or using a mobile.</span>
</div>
  </div>

</template>

<script>

import Header from './components/header.vue'
import story from './components/story.vue'
import feed from './components/feed.vue'
import Nav from './components/nav.vue'
export default {
  name: 'App',
        
  components: {
    Header,
    story,
    feed,
    Nav,
  },
data(){
  return{
    feed: [
      {
        dp: require('./assets/post/dp/a.jpg'),
        Name: 'Dia',
        Location: 'Bar Harbor (US)',  
        post: require('./assets/post/pic/a1.jpg'),
        like: '7k',
        cmt: '159',  
      },
      {
        dp: require('./assets/post/dp/b.png'),
        Name: 'Noah',
        Location: 'Mirfield (UK)',  
        post: require('./assets/post/pic/b1.jpg'),
        like: '5,2k',
        cmt: '82',  
      },
            {
        dp: require('./assets/post/dp/c.png'),
        Name: 'Lisa',
        Location: 'Kitchener (CA)',  
        post: require('./assets/post/pic/c1.jpg'),
        like: '7,3k',
        cmt: '121',  
      },
            {
        dp: require('./assets/post/dp/d.jpg'),
        Name: 'Ben',
        Location: 'Redlands (US)',  
        post: require('./assets/post/pic/d1.jpg'),
        like: '4,3k',
        cmt: '96',  
      },
            {
        dp: require('./assets/post/dp/e.jpg'),
        Name: 'James',
        Location: 'Accrington (UK)',  
        post: require('./assets/post/pic/e1.jpg'),
        like: '6k',
        cmt: '122',  
      },
    ]
  }
}

}
</script>

<style lang="scss">
#app{

  @media (max-width: 576px) {

.alert{
  display: none;
}
  }
 @media (min-width: 576px) {

      .dis{
     display: none;
   }
     
   .alert{
     width: 500px;
     background-color: #FFF4D8;
     //flex-direction: column;
    // margin-top: auto ;
    border-left: 5px solid #FFBA00;
    padding: 10px 0px 10px 25px;
 position: absolute;
  left: 50%;
  top: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
     ;
      
        .n{
 font-size: 25px;
        font-family: 'Roboto', sans-serif;
        //font-weight: bold;
        //margin-left:10px ;
        color: #B78200 ;
        font-weight: 500;
        }
        .txt{
          font-size: 18px;
        font-family: 'Roboto', sans-serif;
        font-weight: 400;
        //margin-left:10px ;
        color: #B78200 ;

        }
   }
 }
}

</style>
