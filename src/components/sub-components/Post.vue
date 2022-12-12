<script setup>
    defineProps({
        post: Object
    })
</script>

<template>
    <div class="post" :id="`post-${post.id}`">
        <div class="header">
            <img :src="post.user.image" />
            <h4>{{post.user.name}}</h4>
        </div>
        <p class="text">
            {{post.text}}
        </p>
        <ul class="images">

        </ul>
    </div>
</template>

<style lang="scss">
    @use '../../styles/abstracts' as *;

    .post{
        .header{
            img{
                font-size: 2rem;
                height: 1em;
                width: 1em;
                border-radius: 1em;
            }
        }
    }
</style>