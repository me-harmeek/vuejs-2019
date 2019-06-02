<template>
<div>
<ul>
  <li v-for="data in datanews">
    <a :href="data" v-bind:name="data">{{data}}</a>
  </li>
</ul>
<h3> {{message}} </h3>
<button v-on:click="harmeek">click me</button>
</div>

</template>

<script>
export default {

    data(){
        return{
            message:'Hello i m haremmk',
            datanews:['news1','news2','news3','news4','news5']
        }
    },
    methods:{
        harmeek:function(){
           this.message = "I am Updated"
        }
    }
}
</script>