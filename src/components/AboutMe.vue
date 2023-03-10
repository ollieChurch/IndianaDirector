<template>
    <div class="row" ref="about">
        <div class="col-md-6 p-0">
            <b-img
                :src="aboutMeImg"
                class="about-img"
                alt="Indiana gives notes during rehearsal for The Last Supper"
            ></b-img>
        </div>
        <div class="col-md">
            <b-container class="py-5 ps-md-1 pe-md-4">
                <h2 class="display-2">About Indiana</h2>
                <p class="pt-2 pb-3">{{ aboutMeText }}</p>

                <div class="d-flex-sm justify-content-around">
                    <b-button
                        variant="custom-primary"
                        size="lg"
                        class="m-2"
                        :href="twitterLink"
                        target="_blank"
                    >
                        Twitter
                        <b-icon-twitter class="ms-2"></b-icon-twitter>
                    </b-button>
                    <b-button
                        variant="custom-primary"
                        size="lg"
                        class="m-2"
                        @click="$emit('goToContact')"
                    >
                        Email
                        <b-icon-envelope-fill
                            class="ms-2"
                        ></b-icon-envelope-fill>
                    </b-button>
                </div>
            </b-container>
        </div>
    </div>
</template>

<script>
    import defaultAboutPic from '../assets/lastSupper.jpeg'

    export default {
        name: 'AboutMe',

        props: ['aboutMeText', 'aboutMeImage', 'twitterLink'],

        data() {
            return {}
        },

        computed: {
            aboutMeImg() {
                const userUpload = this.aboutMeImage
                return userUpload
                    ? userUpload.split('/public').join('')
                    : defaultAboutPic
            }
        }
    }
</script>

<style scoped>
    .about-img {
        overflow: hidden;
        object-fit: cover;
        width: 100%;
        height: 100%;
    }
</style>
