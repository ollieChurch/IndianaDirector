<template>
    <div class="sticky-nav py-3">
        <div class="nav-top"></div>
        <b-container>
            <b-nav fill class="justify-content-center align-items-center nav">
                <b-nav-item @click="handleClick('about')">About</b-nav-item>
                <b-nav-item @click="handleClick('shows')">Shows</b-nav-item>
                <b-nav-item v-if="includePress" @click="handleClick('press')">
                    Press
                </b-nav-item>
                <b-nav-item @click="handleClick('contact')">Contact</b-nav-item>
            </b-nav>
        </b-container>
    </div>
</template>

<script>
export default {
    name: 'navBar',
        
        props: ['includePress'],

        methods: {
            handleClick(refName) {
                this.$emit('navClicked', refName)
            }
        }
    }
</script>

<style scoped>
    .nav {
        font-size: 1.5rem;
    }

    .sticky-nav {
        background: rgba(255, 255, 255, 0.906);
        position: -webkit-sticky !important;
        position: sticky !important;
        top: 0;
        z-index: 10;
        border-bottom: 2px black solid;
    }
</style>
