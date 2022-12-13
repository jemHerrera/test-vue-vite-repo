<script setup>
    import AgeVerification from './components/AgeVerification.vue'
</script>

<template>
    <div class="wrapper">
        <a href="#" class="logo">
            <img src="/images/desktop-logo/desktop-logo.png" />
        </a>
        
        <img class="main-image" srcset="/images/desktop-image/desktop-image.png 1920w, /images/mobile-image/mobile-image.png 800w"
        src="/images/desktop-image/desktop-image.png"
        alt="Coffee & Co. coffe shop with customers"/>


        <AgeVerification id="age-verification" />
    </div>
</template>

<style lang="scss">
@use './styles/abstracts' as *;
@use './styles/resets.scss';

#motiv-component{
    height: 100%;
    width: 100%;
    background: url('/images/desktop-background/desktop-background.png');
    padding: calc(90*100%/1920) calc(140*100%/1080);

    .wrapper{
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-gap: 16px;
        position: relative;

        .main-image{
            height: 100%;
            width: 100%;
            object-fit: contain;
            grid-column: 1 / 8;
        }

        .logo{
            position: absolute;
            top: 0;
            right: 0;
        }
    }
}
</style>
