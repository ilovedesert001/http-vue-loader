
<template>
    <div class="hello" style="color: red">Hello {{who}}</div>
</template>

<script>
    module.exports = {
        data: function() {
            return {
                who: 'world'
            }
        }
    }
</script>

<style>
    .hello {
        background-color: #ffe;
    }
</style>