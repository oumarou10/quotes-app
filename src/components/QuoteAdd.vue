<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-md-4 col-md-offset-3 col-lg-3 form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="6" v-model="quote" @keyup.enter="createNew"></textarea>

            </div>
            <div class="col-sm-8  col-md-4 col-md-offset-3 form-group">
                <button class="btn btn-primary"  @click.prevent="createNew">Add Quote</button>
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
            createNew() {
                this.$emit('quoteWasAdded', this.quote);
                this.quote = ''
            }
        }
    }
</script>

<style scoped>

</style>