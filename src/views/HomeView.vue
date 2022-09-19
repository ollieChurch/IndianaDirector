<template>
    <div>
        <div class="header">
            <b-img
                thumbnail
                rounded="circle"
                :src="profileImg"
                class="profile-img mt-4"
            ></b-img>
        </div>
        <b-container class="py-3">
            <h1 class="display-1">
                Indiana <span class="surname">Lown-Collins</span>
            </h1>
            <h2 class="text-muted pb-3 mb-4"><em>Award-Winning Theatre Director</em></h2>
            <hr />
            <b-nav fill class="justify-content-center mt-3 nav">
                <b-nav-item to="/about">About</b-nav-item>
                <b-nav-item to="/about">Shows</b-nav-item>
                <b-nav-item to="/">Contact</b-nav-item>
            </b-nav>
        </b-container>

        <b-jumbotron
            header='"Theatre has given me strength & light in a world that can feel scary and lonely. The power it has of making people feel seen, heard and understood is like no other"'
            lead="- Indiana Lown-Collins -"
            fluid
            class="jmk-jumbotron text-white py-5"
        >
            <p class="mt-5">Indiana won the prestigious JMK award for emerging theatre directors in 2022. The above quote is from her acceptance speech.</p>
            <b-button size="lg" variant="primary" href="#">Find Out More</b-button>
        </b-jumbotron>

        <b-container class="py-4">
            <b-card
                title="About Me"
                :img-src="lastSupperImg"
                img-top
            >
                <b-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed in orci eu velit commodo cursus. Vestibulum vitae blandit magna. Aenean ac tincidunt nisl. Integer efficitur viverra turpis ac volutpat. Quisque at ipsum ut nisl tempor molestie. Aenean lobortis ipsum nec blandit iaculis. Nulla maximus iaculis lacus eget blandit. Donec lacus nisl, dignissim sed ullamcorper cursus, iaculis convallis sem. Nam varius odio et bibendum auctor. Duis ut efficitur felis.</b-card-text>
                <div class="d-flex justify-content-around">
                    <b-button variant="primary" size="lg" class="mt-2">
                        Twitter
                        <b-icon-twitter class="ms-2"></b-icon-twitter>
                    </b-button>
                    <b-button variant="primary" size="lg" class="mt-2">
                        Email
                        <b-icon-envelope-fill class="ms-2"></b-icon-envelope-fill>
                    </b-button>
                </div>
                
            </b-card>
        </b-container>
    </div>
</template>

<script>
import profilePic from '../assets/profilePic.jpeg'
import jmkImage from '../assets/jmk.jpeg' 
import woodsImage from "../assets/woods.jpeg"
import globeImage from "../assets/globe.jpeg"
import lastSupperImage from "../assets/lastSupper.jpeg"



    export default {
        name: 'HomeView',

        data: function () {
            return {
                profileImg: profilePic,
                jmkImg: jmkImage,
                woodsImg: woodsImage,
                globeImg: globeImage,
                lastSupperImg: lastSupperImage
            }
        }
    }
</script>

<style scoped>
    .header {
        /* background: linear-gradient(
            0deg,
            rgba(255, 254, 254, 1) 0 18%,
            rgba(0, 212, 255, 1) 0 100%
        ); */
        background: black;
        background-image: url(../assets/globe.jpeg);
        background-size: cover;
        max-height: 230px;
    }
    .profile-img {
        height: 250px;
        aspect-ratio: 1/1;
    }

    .nav {
        font-size: 1.5rem;
    }

    .surname {
        white-space: nowrap;
    }

    .jmk-jumbotron {
        background: rgba(0, 0, 0, 0.395);
        background-image: url(../assets/jmk.jpeg);
        background-size: cover;
        background-position: center;
        background-blend-mode: darken;
    }

    h1 {
        margin-top: 2rem;
        margin-bottom: 0;
    }
</style>
