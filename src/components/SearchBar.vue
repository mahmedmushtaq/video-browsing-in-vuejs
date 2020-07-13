<template>
    <div class="m-5 text-center">
        <input @input="onInput"/>
    </div>
</template>

<script>

    export default{
        name:'SearchBar',
        methods:{
            onInput: function(e) {
                 this.$emit('termChange',e.target.value)
            }
        }

    }
</script>

<style scoped>
    input{
        width:75%;

    }
</style>
