<script setup>
    import { reactive } from 'vue';
    import Header from '../main-components/Header.vue'
    import Body from '../main-components/Body.vue'
    
    const STATIC_POSTS = [
        {
            user: {
                name: 'Camille',
                image: '/images/pixelpfp-camille-color.jpg'
            },
            id: '1212221300',
            date: 'Dec 12 2022, 1:00pm',
            text: `
                DANG❗️Ok, so i heard about @GigaDAOio in a conversation between two friends a few days ago. 
                Since then i've read all about their upcoming product GigaDEX, the first exchange for Solana NFT's, and am now 100% positive that y'all want to be early on this. 
            `,
            images:{

            }
        },
        {
            user: {
                name: 'Eric',
                image: '/images/pixelpfp-eric.jpg'
            },
            id: '1212221232',
            date: 'Dec 12 2022, 12:32pm',
            text: `We are building a diverse, active, and engaged community of long-term investors who will be loudest and strongest together.`,
            images:{

            }
        },
        {
            user: {
                name: 'Damien',
                image: '/images/pixelpfp-damien-1.jpg'
            },
            id: '1212221120',
            date: 'Dec 12 2022, 11:20pm',
            text: `NEWS: 🌱 H&M is using Snapchat's augmented reality "try-on" experiences to promote digital fashion and explore new sustainability options.`,
            images:{

            }
        }
    ]

    const posts = reactive([...STATIC_POSTS]);
</script>

<template>
    <div id="home">
        <Header />
        <Body 
            :posts="posts"
        />
        <div class="new-post-container">
            <a id="new-post-button" href="#/new-post">Create New Post</a>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../../styles/abstracts' as *;

    #home{
        @include flex($direction:column);
        height: 100%;

        #body{
            flex-grow: 1;
        }

        .new-post-container{
            position: fixed;
            bottom: 0;
            @include flex($align:center, $justify:center);
            padding: 1em;
            width: 100%;

            #new-post-button{
                padding: 0.75em 1.5em;
                background: $color-main;
                color: white;
                border-radius: 99em;
                text-decoration: none;
                font-size: 1.25rem;
                font-weight: 600;

            }
        }
    }
</style>