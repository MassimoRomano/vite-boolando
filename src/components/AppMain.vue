<script>
/* import { products } from '../product'; */
import BodyCard from './BodyCard.vue';
import { state } from '../state.js'

export default {
    name: 'AppMain',
    components: {
        BodyCard
    },
    data() {
        return {
            state
        }
    },
    mounted() {
           this.state.getProducts(this.state.base_products_api_url)
    }
}
</script>

<template>
    <div class="container">
        <div class="row my-4">
            <!-- Itera sui prodotti e li inserisce in colonne -->
            <div class="col-4 mb-4" v-for="product in state.products" :key="product.id">
                <BodyCard :product="product" />
            </div>
        </div>
        <p>Ci sono: {{ state.products.length }} capi</p>
    </div>
</template>

<style></style>