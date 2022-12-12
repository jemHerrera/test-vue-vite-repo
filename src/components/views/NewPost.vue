<script setup>
</script>

<template>
    <div id="new-post">
        <a href="/"><span class="material-icons">arrow_back</span></a>
        <div>Hello from NewPost</div>
    </div>
</template>

<style lang="scss">
    @use '../../styles/abstracts' as *;

    #new-post{
        position: absolute;
        height: 100vh;
        width: 100vw;
        top:0;
        left:0;
    }
</style>