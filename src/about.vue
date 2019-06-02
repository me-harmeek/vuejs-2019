<template>
<div>
<h1>Hi i m rabindra</h1>
<h4>{{AboutTitle}}</h4>
<button type="button" @click="dataChange">Click button</button>
<h5> Name: {{name}}</h5>
<h6>myplaylist : {{myplaylist}}</h6>
</div>
</template>

<script>
    export default{
        props:['name','myplaylist'],
        data(){
            return{
                about : 'Hi Harmeek jee',
                AboutTitle : 'Hiiiiiii'
            }
        },
        methods:{
            dataChange:function(){
                this.AboutTitle ="Data updated"
            }
        }
    }
</script>