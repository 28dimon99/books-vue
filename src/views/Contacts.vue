<template>
    <div class="row">
        <div class="col s6 offset-s3">
            <h1>Create task</h1>
            <form  action="">
                <div class="input-field">
                    <input v-model="title" type="text" id="title" class="validate" required>
                    <label for="title">Title</label>
                    <span class="helper-text" data-error="Title is required"></span>
                </div>
                <div class="chips" ref="chips"></div>

                <div class="input-field">
                    <textarea v-model="description" id="description" class="materialize-textarea"></textarea>
                    <label for="description">Description</label>
                    <span class="character-counter"
                          style="float: right; font-size: 12px">{{description.length}}/2048</span>
                </div>

                <input type="text" ref="datepicker">

                <button class="btn" type="submit">Create task</button>

            </form>
        </div>
    </div>
</template>

<script>


    export default {
        name: 'Create',
        data: () => ({
            description: '',
            title: '',
            chips: null,
            date: null
        }),
        mounted() {
            this.chips = M.Chips.init(this.$refs.chips, {
                placeholder: 'Task tags'
            });
            this.date = M.Datepicker.init(this.$refs.datepicker, {
                format: 'dd.mm.yyyy',
                defaultDate: new Date(),
                setDefaultDate: true
            })
        },
        methods:{

        },
        components: {}
    }
</script>
