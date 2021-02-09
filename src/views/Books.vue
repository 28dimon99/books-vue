<template>
    <div>
        <div class="content"
             v-for="book in BOOKS"
             :key="book.id"
             :books="books"
        >
            <div>
                <img :src="book.image">

            </div>

            <div class="card-action">
                <strong>{{book.autor}}</strong>
            </div>

            <div class="card sticky-action">
                {{book.name}}
            </div>
            <div>
                Ціна: {{book.price}} грн
            </div>
            <button>Купити</button>

        </div>
        <router-view/>
    </div>
</template>

<script>
    import { mapGetters, mapActions } from "vuex";


    export default {
        name: "Home",
        computed: mapGetters(['BOOKS']),
        methods: mapActions(["GET_BOOKS_FROM_API"]),
        components: {},
        mounted() {
            //вызов action
            this.GET_BOOKS_FROM_API();
        }
    };
</script>

<style scoped>

</style>