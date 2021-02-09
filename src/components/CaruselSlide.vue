<template>
    <div class="v-carusel-item">
    <img src='../assets/image/carusel/1.png'/>

    </div>
</template>

<script>
    export default {
        name: "Carusel-item",
        props:{
            item_data:{
                type: Object,
                default: ()=>[]
            }
        },
        data(){
            return{

            }
        },
        computed:{

        }

    }
</script>

<style scoped>

</style>