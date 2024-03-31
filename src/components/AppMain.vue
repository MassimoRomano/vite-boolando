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
            state,
            showModal: false,
            selectedImage: ''
        }
    },
    methods: {
        openModal(product) {
            this.selectedImage = product;
            this.showModal = true;
        },
        closeModal() {
            this.showModal = false;
            this.selectedImage = '';
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
            <div class="col-4 mb-4" v-for="product in state.products" :key="product.id">
                <BodyCard :product="product" @open-modal="openModal"/>
            </div>
        </div>
        <p>Ci sono: {{ state.products.length }} capi</p>

        <div class="modale" v-if="showModal">
            <div class="modale-content">
                <span class="close" @click="closeModal">&times;</span>
                <div class="modale-body">
                    <img :src="selectedImage" alt="Product Photo" class="center-image" />
                </div>
            </div>
        </div>
    </div>
</template>


<style scoped lang="scss">


</style>