<template>
    <div class="container">
        <h1>
            Content goes here
        </h1>
    </div>
</template>
<script>
export default {
    name: 'AppMain',
    data() {
        return {

        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as*;
@use '../styles/partials/variables' as*;

div.container{
    background-color: black;
}
h1{
    font-size: 1.5rem;
    color: white;
}
</style>