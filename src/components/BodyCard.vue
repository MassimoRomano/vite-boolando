<script>

export default {
  name: 'BodyCard',
  props: {
    product: Object
  },
  data() {
    return {
      hovering: false
    }
  },
  methods: {
    toggleHover(status) {
      this.hovering = status;
    }
  },
  computed: {
    hasDiscount() {
      return this.product.badges.some(badge => badge.type === 'discount')
    },
    discountedPrice() {
      if (this.hasDiscount) {
        const discountBadge = this.product.badges.find(badge => badge.type === 'discount');
        const discountPercentage = parseFloat(discountBadge.value) / 100;
        return (this.product.price * (1 - discountPercentage)).toFixed(2);
      }
      else {
        return this.product.price;
      }
    }
  }
}
</script>