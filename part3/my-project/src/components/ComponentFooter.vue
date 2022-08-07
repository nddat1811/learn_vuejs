<template>
    <header>
        <h1> {{ title }}</h1>
    </header>
</template>

<script>
export default {
    name: 'comp-footer',
    props: {
        title: String,
    },
    data() {
        return {
            text: 'Footer',
        }
    },
}
</script>

<style>
</style>