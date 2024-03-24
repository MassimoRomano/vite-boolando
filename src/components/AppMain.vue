<script>
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