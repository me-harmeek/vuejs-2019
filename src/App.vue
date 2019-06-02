<template>
  <div id="app">
    <div class="container">
     <Header></Header>


      <div class="row section-area">
          <div class="col-sm-4">
            <aside>
              <News></News>
            </aside>
          </div>
          <div class="col-sm-8">
            <Services></Services>
          </div>
      </div>

      
      <Footer>

      </Footer>
    </div>
  </div> 
</template>

<script>
import Header from './components/header.vue';
import Footer from './components/footer.vue';
import News from './components/news.vue';
import Services from './components/services.vue';

export default {
  components:{
    Header,
    Footer,
    News,
    Services
  }
}



</script>

<style lang="scss">
.container{
  header{
    background: gray;
  }
  aside{
    border-right:2px solid gray;
    height:100%;

  }
  .section-area{
    img{
     margin:30px 0;
    }
  }
  footer{
    background: #000;
    color:#fff;
  }

  .products{
    border:1px solid gray;
    width:100%;
    padding:10px;
    margin:15px 0;
    img{
      height:auto;
      width:100%;
    }
    h6{
      border-top:1px solid red;
      margin-top:10px;
    }
  }
}
  
</style>
