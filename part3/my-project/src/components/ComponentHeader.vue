<template>
    <header>
        <h1> {{ title }} <br>
            <button v-on:click="changeTittleHeader">
                Thay đổi tittle từ Component Header.vue
            </button>

        </h1>

    </header>
</template>

<script>
export default {
    name: 'comp-header',
    props: {
        title: {
            type: String,
            default: "sso"
        }
    },
    data() {
        return {
        }
    },
    methods: {
        changeTittleHeader(e) {
            let data = {
                title: "transfer title ne"
            }
            this.$emit('changeTitleEvent', data)
        } 
    }
}
</script>

<style>
</style>