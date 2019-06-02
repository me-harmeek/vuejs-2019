<template>
<div>
    <div class="row">
        <div class="col-sm-4" v-for="data in images">
            <img :src="getImgUrl(data)"  class="img-fluid">
        </div>
    </div>

    <div class="row">
        <div class="col-sm-4" v-for="product in productDetail">
            <div class="products">
                <img :src="getImgUrl(product.imgpath)" v-on:click="selectImage(product.id,product.price)" />
                <h6>{{product.description}}</h6>
                <p>{{ product.color}}</p>
                <p>price :{{product.price}}</p>
                <p>{{product.id}}</p>
            </div>
        </div>
    </div>
</div>
</template>

<script>

export default {

data(){
    return{
        images:['home-4.png','store_profile.png','target_report.png','team.png'],
        productDetail:[
        {
            id:1,
            imgpath:'home-4.png',
            price:500,
            description:'Shirt',
            color:'black'
        },
        {
            id:2,
            imgpath:'store_profile.png',
            price:1500,
            description:'Jeans' ,
            color:'black'
        },
         {
            id:3,
            imgpath:'target_report.png',
            price:2500,
            description:'Watch',
            color:'Red'
        },
        {
            id:4,
            imgpath:'team.png',
            price:4500,
            description:'Computer',
            color:'Green'
        }
       
        ]
    }
},
methods:{
  getImgUrl(services) {
    return services ? require(`../assets/images/${services}`) :''
  },
   selectImage:function(id,pro) {
      alert(id);
      alert(pro);
    }
}

}

</script>