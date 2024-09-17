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
            type:Number,
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
    <h3>
        SeriesListCard
        {{ seriesName }}}
    </h3>

</template>

<style lang="scss" scoped>
  
</style>
