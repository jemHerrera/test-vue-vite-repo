<script setup>
</script>

<template>
    <header>
        <span class="material-icons icon-settings">settings</span>
        <h1 id="logo">Post App</h1>
        <img class="profile-picture" src="/images/pixelpfp.jpg" />
    </header>
</template>

<style lang="scss">
    @use '../../styles/abstracts' as *;


    header{
        @include flex($justify:space-between);
        padding: 1rem;
        
        .material-icons{
            font-size: 2rem;
        }

        .profile-picture{
            font-size: 2rem;
            height: 1em;
            width: 1em;
            border-radius: 1em;
        }
    }

</style>