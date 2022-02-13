<template>

    <div class="container">  
        <h4>Credit-card input:</h4>
        <credit-card 
        v-model:nameOnCard="nameOnCard"
        v-model:cardNumber="cardNumber"
        v-model:expiry="expiry"
        v-model:cvv="cvv"
        >

        </credit-card>
        <br>
        <hr>
        <br>
        <p>
           <strong>Name: </strong> {{nameOnCard}} <br>
            <strong>Card Number: </strong> {{cardNumber}}<br>
            <strong>Expiry: </strong> {{expiry}}<br>
            <strong>CVV: </strong> {{cvv}}
        </p>
        
    </div>
    
    
</template>

<script>
import CreditCard from './components/CreditCard.vue'

export default {
    data(){
        return {
            myRating: 4,
            nameOnCard: "Mohammad Parvaz",
            cardNumber: "",
            expiry: "",
            cvv: ""
          
        };
    },

    methods:{

    },        

    components: {
        CreditCard,
        
    }

}
</script>

<style>
.container{
    padding: 22px;;
}

</style>

