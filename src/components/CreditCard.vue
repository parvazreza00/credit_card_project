<template>
<div class="credit-card">
    <label for="">Name on Card</label><br>
    <input type="text" placeholder="Mohammad parvaz" :value="nameOnCard" @input="handleClick('update:nameOnCard', $event)">
    <br>
    <label for="">Card Number</label><br>
    <input type="text" placeholder="0000-0000-0000" :value="cardNumber" @input="handleClick('update:cardNumber', $event)">
    <br>
    <div class="row">
        <div class="col-6">
            <label for="">Expired date</label><br>
    <input type="text" placeholder="mm/yy" :value="expiry" @input="handleClick('update:expiry', $event)">
        </div>
        <div class="col-6">
            <label for="">CVV</label><br>
    <input type="text" placeholder="000-000-000" :value="cvv" @input="handleClick('update:cvv', $event)">
        </div>
    </div>
    
    
    

</div>
  
</template>

<script>
export default {
    props:{
        nameOnCard: {
            type:String,
            default: ""
        },
        cardNumber: {
            type:String,
            default: ""
        },
        expiry: {
            type:String,
            default: ""
        },
        cvv: {
            type:String,
            default: ""
        }
    },
    methods:{
        handleClick(eventName, e){
            this.$emit(eventName,e.target.value);
        }
    }

}
</script>

<style>

.credit-card{
    width:288px;
    border:1px solid gray;
    padding: 22px;
    border-radius:5px;
    background-color: rgb(255, 254,247);
    color:rgb(82,82,82);
    min-height: 111px;

}

input{
    padding: 7px 9px;
    margin-bottom: 11px;
    border-radius: 3px;
    width: 100%;
    border:1px solid gray;

}

.row{
    display:flex;

}

/* .col-6{
    flex:.1;
    padding: 0.2px;
} */

</style>