<script setup>
    import { computed } from 'vue';
    
    const MIN_YEAR = 1900;
    const CURRENT_YEAR = 2022;

    const years = computed(()=>{
        let array = [];

        for(let i = MIN_YEAR; t<=CURRENT_YEAR; i++){
            array.push(i);
        }

        return array;
    })

</script>

<template>
    <div>
        <h2>Joining us for <span class="main-color1">coffee</span> or <span class="main-color2">late night cocktails?</span></h2>
        <p><i>Please verify that you are 18 years of age or older to enter the site.</i></p>
        <form>
            <div class="selections">
                <select class="Day">
                    <option value="" disabled selected>Day</option>
                </select>
                <select class="month">
                    <option value="" disabled selected>Month</option>
                </select>
                <select class="Year">
                    <option value="" disabled selected>Year</option>
                </select>
            </div>
            <button class="submit">Enter Site</button>
        </form>
    </div>
</template>

<style lang="scss">

    @use '../styles/abstracts' as *;

    #age-verification{
        @include flex($direction: column, $gap: 1.5em);
        background: white;
        grid-column: 6 / 13;
        width: 100%;
        position: absolute;
        // harcoded :D
        bottom: 20%;
        box-shadow: 0px 10px 30px #9A558029;
        padding: 50px;
        border-radius: 50px;

        h2{
            font-weight: bold;
            font-size: 2.5rem;
        }

        form{
            @include flex($direction:column, $gap: 2em, $align:flex-start);

            .selections{
                @include flex($gap: 1.5em);
                select{
                    font-size: 1.15em;
                    padding: 0.5em 1em;
                    border: 1px solid #7C7C7C;
                    border-radius: 10px;
                    color: #7C7C7C;
                }
            }

            .submit{
                font-size: 1.25em;
                padding: 0.75em 1.25em;
                border-radius: 99em;
                background: $color-gscale1;
                letter-spacing: 0px;
                color: #FFFFFF;
                opacity: 1;
                font-weight: bold;
            }
        }

    }
</style>