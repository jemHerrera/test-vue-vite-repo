<script setup>
    import Post from '../sub-components/Post.vue' 

    defineProps({
        posts: Array
    })
</script>

<template>
    <main id="body">
        <ul class="posts">
            <Post 
                v-for="post in posts" :key="post.id"
                :post="post"
            />
        </ul>
    </main>
</template>

<style lang="scss">
    @use '../../styles/abstracts' as *;

    #body{
        overflow: auto;
    }
</style>