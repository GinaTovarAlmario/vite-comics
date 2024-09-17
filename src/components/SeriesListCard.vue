<script>
export default {
    data() {
        return {
            
            
        }
    },
    props:{
        seriesThumb:{
           type: String,
           required:true,
        },
        seriesPrice:{
            type: String,
            required:false,
        },
        seriesName:{
            type:String,
            required:true,
        },
        seriesType:{
            type:String,
            required:false,
        }
    }
}
</script>
<template>
    <article>
        <img :src="seriesThumb" :alt="seriesName">
        <h3>
            {{ seriesName }}
        </h3>
    </article>    
</template>

<style lang="scss" scoped>
article{
    width: calc( 100% / 6 - 20px);
    height: 250px;
    padding-bottom: 20px;

    img{
        height: 200px;
        width: 300px;
    }

    h3{
        text-align: center;
        font-size: 16px;
    }
}
    
  
</style>
