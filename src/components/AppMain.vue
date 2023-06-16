<template>
    <main>
      <div class="container">
        <h1>
            Content goes here
        </h1>
      </div>
    </main>
    
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

main{
    height: $sectionsHeight;
    @include flex(row,center,center,nowrap);
    background-color: black;
    
    h1{
      font-size: 1.5rem;
      color: white;
      padding-left: 35px;
    }
}


</style>