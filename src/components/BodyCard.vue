<script>
export default {
  name: 'BodyCard',
  props: {
    product: Object
  },
  methods: {
    hasDiscount(product) {
      return product.badges.some(badge => badge.type === 'discount');
    },
    discountedPrice(product) {
      if (this.hasDiscount(product)) {
        const discountBadge = product.badges.find(badge => badge.type === 'discount');
        const discountPercentage = parseFloat(discountBadge.value) / 100;
        return (product.price * (1 - discountPercentage)).toFixed(2);
      } else {
        return product.price;
      }
    }
  }
}
</script>

<template>
  <div class="card border border-0">
    <img :src="product.frontImage" class="card-img-top trans-front" alt="...">
    <img :src="product.backImage" class="card-img-top trans-back" alt="...">
    <h6>{{ product.brand }}</h6>
    <h6 class="fw-bolder">{{ product.name }}</h6>
    <p v-if="hasDiscount(product)" class="mb-0">
      <span class="text-danger fw-bolder">{{ discountedPrice(product) }}€</span>
      <span class="text-secondary text-decoration-line-through">{{ product.price }}€</span>
    </p>
    <p v-else>{{ product.price }} €</p>
    <div v-for="(badge, index) in product.badges" :key="index" class="card-badge">
      <p :class="{ 'sost-2': badge.type === 'tag', 'disc': badge.type === 'discount' }">
        {{ badge.value }}
      </p>
      <i class="fa-solid fa-heart heart"></i>
    </div>
  </div>
</template>
