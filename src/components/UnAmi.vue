<template>
    <div class="container my-1">
        <ul class="list-group">
            <h2 class="list-group-item">{{leNom}} {{premiumData ==='1'? 'Ami premium':'Ami nul'}}</h2> 
            <button @click="afficherPremium" class="btn btn-danger">Premium ?</button>
            <button @click="afficherDetails" class="btn btn-primary">{{detailsVisibles? 'Masquer': 'Afficher'}}</button>           
            <ul v-if="detailsVisibles" class="list-group">
                <li class="list-group-item">{{lePhone}}</li>
                <li class="list-group-item">{{leMail}}</li>
            </ul>
        </ul>
    </div> 
</template>

<script lang='js'>
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'UnAmi',
    props:{
        leNom:{
            type:String,
            required:true
            // required:false,
            // default:'NomParDefaut'
        },
        lePhone:{
            type:String,
            required:true
        },
        leMail:{
            type:String,
            required:true
        },
        premium:{
            type:String,
            required:false,
            default:'0',
            validator: function(value){return value==='1' || value==='0'}
        }
    },
    data() {
        return {
            detailsVisibles:false,
            premiumData: this.premium

        };
    },

    methods: {
        afficherDetails(){
            this.detailsVisibles = !this.detailsVisibles;
        },
        afficherPremium(){
            if (this.premiumData==='1') {
                this.premiumData='0'
            } else {
                this.premiumData='1'
            }
        }
    },
});
</script>