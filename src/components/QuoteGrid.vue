<template>
    <div class="row">
        <single-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</single-quote>
    </div>
</template>

<script>
    import Quote from './Quote.vue';
    export default {
        props: ['quotes'],
        components: {
            singleQuote: Quote
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index);
            }
        }
    }
</script>

<style>

</style>
