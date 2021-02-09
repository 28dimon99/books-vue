<template>
    <div>

        <CartItem>

        </CartItem>
    </div>

</template>

<script>

    import {mapGetters} from "vuex";
    import CartItem from "../components/CartItem";

    export default {
        name: "Cart",
        computed:{
            ...mapGetters([''])
        },
        components:{
            CartItem
        }
    }
</script>

<style scoped>

</style>