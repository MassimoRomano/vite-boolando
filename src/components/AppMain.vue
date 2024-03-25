<script>
import axios from 'axios';
import { products } from '../product';
import BodyCard from './BodyCard.vue';


export default {
    name: 'AppMain',
    components: {
        BodyCard
    },
    data() {
        return {
            products
        }
    },
    mounted (){
        axios.get('http://localhost:3000/products')
        .then(response =>{
            console.log(response)
            this.products = response.data
        })
    }
}
</script>

<template>
    <div class="container">
        <div class="row my-4">
            <!-- Itera sui prodotti e li inserisce in colonne -->
            <div class="col-4 mb-4" v-for="product in products" :key="product.id">
                <BodyCard :product="product" />
            </div>
        </div>
    </div>
</template>

<style></style>