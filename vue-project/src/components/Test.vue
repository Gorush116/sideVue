<template>
    <h1>{{ msg }}</h1>
    <h2>{{ msg2 }}</h2>
    <h3 v-html="rawHtml"/>
</template>

<script>
export default {
    name: "",
    props: {
        msg: {
            type: String,
            required: true
        }
    },
    mixins: [],
    components: {},
    data() {
        return {
            msg2: "나는 Vue다!",
            rawHtml: "html태그 안이지롱",
            bindId: "bid"
        }
    },
    methods: {

    },
    created() {
        
    },
    mounted() {

    },
    activated() {

    }
}
</script>

<style scoped>

</style>