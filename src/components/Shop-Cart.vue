<template>
    <div class="Cart">
        <p>Kurv: {{this.cart.length}} frugter</p>
        <!-- Button component -->
        <Shop-Button-Empty
                @emit-empty-cart="emitEmptyCart">
            <p>Tøm kurv</p>
        </Shop-Button-Empty>
        <p>Total: {{this.total}} Kr</p>
    </div>
</template>

<script>
import ShopButtonEmpty from './Shop-Button-Empty.vue'

    export default {
        name: 'Shop-Cart',
        components: {ShopButtonEmpty},
        props: ['cart', 'total'],
        data() {
            return {}
        },
        methods: {
            emitEmptyCart() {
                this.$emit('empty-cart')
            }
        }
    }
</script>

<style>

</style>
