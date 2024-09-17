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
    <div>
       <img :src="seriesThumb" :alt="seriesName">
    </div>
    <h3>
        {{ seriesName }}
    </h3>
</template>

<style lang="scss" scoped>
  
</style>
