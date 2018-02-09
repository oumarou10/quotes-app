<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-md-4 col-md-offset-3 col-lg-3 form-group">
                <label>Quote</label>
                <text-area class="form-control" v-model="quote"></text-area>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-md-4 col-md-offset-3 col-lg-3 form-group">
                <button class="btn btn-primary" @click="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        name: "quote-add",
        data: function () {
            return {
                quote: ''
            }
        },
        methods: {
            createNew(){

            }
        }
    }
</script>

<style scoped>

</style>