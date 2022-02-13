<template>
    <div class="product-card">
        <div class="product-card__title">
           {{product.name}}
        </div>
        <div class="product-card__body">
              <img :src="product.thumnail" alt="">
              <p>{{product.price}}</p>         
        </div>
        <div class="product-card__footer">
            <button @click="handleBuyNow">BuyNow</button>
            <button>Add To Card </button>

        </div>
    </div>
  
</template>

<script>
export default {
    props: {
        product: {
            type: Object,
            default: ()=>({})
        }
    },
    methods:{
        handleBuyNow(){
            this.$emit("buy-now-click");
        }
    }

}
</script>

<style>
.product-card{
    width:200px;
    border: 1px solid #006f88;
    min-height: 200px;
    margin:22px;
}
.product-card__title{
    background: #167db1;
    padding:5px 11px;
    color:#fff;
}
.product-card__body{
    padding: 11px;
    text-align: center;

}
.product-card__body img{
    height: 111px;
    
}
.product-card__footer{
    text-align: center;
    margin-bottom:10px;
}
.product-card__footer button{
    margin-right: 4px;
    padding:5px;
    
}

</style>