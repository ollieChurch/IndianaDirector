<template>
    <b-jumbotron
        header="Theatre has given me strength & light in a world that can feel scary and lonely. The power it has of making people feel seen, heard and understood is like no other"
        lead="- Indiana Lown-Collins -"
        fluid
        class="jmk-jumbotron text-white py-5"
    >
        <p class="mt-5">
            Indiana won the prestigious JMK award for emerging theatre directors
            in 2022. The above quote is from her acceptance speech.
        </p>
        <b-button
            size="lg"
            variant="custom-primary"
            href="https://www.jmktrust.org/2022/07/jmk-award-winner-2022/"
            target="_blank"
        >
            Find Out More
        </b-button>
    </b-jumbotron>
</template>

<script>
    import jmkImage from '../assets/jmk.jpeg'

    export default {
        name: 'JmkAward',

        data() {
            return {
                jmkImg: jmkImage
            }
        }
    }
</script>

<style >
    .jmk-jumbotron {
        background: rgba(0, 50, 61, 0.698);
        background-image: url(../assets/jmk.jpeg);
        background-size: cover;
        background-position: center;
        background-blend-mode: darken;
    }
</style>
