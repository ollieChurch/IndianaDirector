<template>
    <div>
        <header>
            <b-img
                thumbnail
                rounded="circle"
                :src="profileImg"
                class="profile-img mt-4"
                alt="Indiana"
            ></b-img>
        </header>
        <b-container>
            <h1 class="display-1 mt-5 mb-0">
                Indiana <span class="surname">Lown-Collins</span>
            </h1>
            <h2 class="text-muted pb-3 mb-3">
                <em>Award-Winning Theatre Director</em>
            </h2>
        </b-container>
        <div class="sticky-nav py-3">
            <div class="nav-top"></div>
            <b-container>
                <b-nav
                    fill
                    class="justify-content-center align-items-center nav"
                >
                    <b-nav-item @click="scrollMeTo('about')">About</b-nav-item>
                    <b-nav-item @click="scrollMeTo('shows')">Shows</b-nav-item>
                    <b-nav-item @click="scrollMeTo('press')">Press</b-nav-item>
                    <b-nav-item @click="scrollMeTo('contact')">Contact</b-nav-item>
                </b-nav>
            </b-container>
        </div>

        <b-jumbotron
            header='"Theatre has given me strength & light in a world that can feel scary and lonely. The power it has of making people feel seen, heard and understood is like no other"'
            lead="- Indiana Lown-Collins -"
            fluid
            class="jmk-jumbotron text-white py-5"
        >
            <p class="mt-5">
                Indiana won the prestigious JMK award for emerging theatre
                directors in 2022. The above quote is from her acceptance
                speech.
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

        <div class="row" ref="about">
            <div class="col-md">
                <b-img
                    :src="lastSupperImg"
                    class="about-img"
                    alt="Indiana gives notes during rehearsal for The Last Supper"
                ></b-img>
            </div>
            <div class="col-md">
                <b-container class="py-5 ps-md-1 pe-md-4">
                    <h2 class="display-2">About Indiana</h2>
                    <p class="pt-2 pb-3">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed in orci eu velit commodo cursus. Vestibulum vitae blandit magna. Aenean ac tincidunt nisl. Integer efficitur viverra turpis ac volutpat. Quisque at ipsum ut nisl tempor molestie. Aenean lobortis ipsum nec blandit iaculis. Nulla maximus iaculis lacus eget blandit. Donec lacus nisl, dignissim sed ullamcorper cursus, iaculis convallis sem. Nam varius odio et bibendum auctor. Duis ut efficitur felis.
                    </p>
                
                    <div class="d-flex-sm justify-content-around">
                        <b-button 
                            variant="custom-primary" 
                            size="lg" 
                            class="m-2" 
                            href="https://twitter.com/indianalown" 
                            target="_blank"
                        >
                            Twitter
                            <b-icon-twitter class="ms-2"></b-icon-twitter>
                        </b-button>
                        <b-button 
                            variant="custom-primary" 
                            size="lg" 
                            class="m-2"
                            @click="scrollMeTo('contact')"
                        >
                            Email
                            <b-icon-envelope-fill class="ms-2"></b-icon-envelope-fill>
                        </b-button>
                    </div>
                </b-container>
            </div>
        </div>
        
        <div class="py-4 featured-shows-wrapper bg-opacity-50"> 
            <b-container ref="shows">
                <h2 class="display-2">Featured Shows</h2>
                <div class="row">
                    <div class="col-lg my-3" v-for="show in featuredShows" :key="`${show.title}-card`" >
                        <b-card 
                            :img-src="show.image" 
                            :img-alt="show.imageAlt" 
                            img-top
                            class="featured-show-card featured-show-card-height"
                        >
                            <b-card-body class="d-flex flex-column justify-content-between featured-show-card-height">
                                <div>
                                    <b-card-title>{{ show.title }}</b-card-title>
                                    <b-card-sub-title class="mb-3">{{ show.company }}</b-card-sub-title>
                                </div>

                                <b-card-text>{{ show.description }}</b-card-text>
                                <b-card-text class="small">Image Copyright: {{ show.imageCopyright }}</b-card-text>
                            </b-card-body>
                        </b-card>
                    </div>
                    
                </div>
                
                <b-button 
                    size="lg" 
                    variant="custom-secondary" 
                    class="my-4" 
                    href="https://www.linkedin.com/in/indiana-lown-collins" 
                    target="_blank"
                >
                    See Full CV
                    <b-icon-file-earmark-medical-fill class="ms-2"></b-icon-file-earmark-medical-fill>
                </b-button>
            </b-container>
        </div> 

        <div ref="press">
            <b-container class="py-4 px-4 px-md-0">
                <h2 class="display-2">Press & Articles</h2>
                <div class="row justify-content-center py-3 px-2 my-3 press-card">
                    <div class="col-sm align-self-center">
                        <b-card-title class="press-text">"This is a key quote from the article"<span class="text-muted small"> this is the publisher</span></b-card-title>
                    </div>
                    <b-button class="col-sm-2 mt-2 mt-sm-0 align-self-center" variant="custom-primary">Read</b-button>
                </div>

                <div class="row justify-content-center py-3 px-2 my-3 press-card">
                    <div class="col-sm align-self-center">
                        <b-card-title class="press-text">"This is a longer key quote from the article which is really good"<span class="text-muted small"> publisher</span></b-card-title>
                    </div>
                    <b-button class="col-sm-2 mt-2 mt-sm-0 align-self-center" variant="custom-primary">Read</b-button>
                </div>
            </b-container>
        </div>
        
        <div class="pt-4 pb-3 footer-wrapper">
            <b-container ref="contact">
                <h2 class="display-2 text-white">Get In Touch</h2>
                <b-form 
                    class="contact-form" 
                    name="contact" 
                    method="post"
                    data-netlify="true"
                    data-netlify-honeypot="bot-field"
                >
                    <input type="hidden" name="form-name" value="contact" />
                    <b-input 
                        class="my-3" 
                        placeholder="Name" 
                        name="name" 
                        autocomplete="name" 
                        v-model="contactForm.name"
                    ></b-input>
                    <b-input 
                        class="my-3" 
                        placeholder="Email" 
                        name="email" 
                        type="email" 
                        autocomplete="email" 
                        v-model="contactForm.email"
                    ></b-input>
                    <b-textarea class="my-3" placeholder="Message" name="message" v-model="contactForm.message"></b-textarea>
                    <b-button variant="custom-primary" type="submit">Submit</b-button>
                </b-form>

                <div class="site-info mt-4">
                    <p class="my-0">Copyright 2022</p>
                    <p class="my-0">Website built and maintained by Ollie C</p>
                </div>
            </b-container>
        </div>
    </div>
</template>

<script>
    import profilePic from '../assets/profilePic.jpeg'
    import jmkImage from '../assets/jmk.jpeg'
    import globeImage from '../assets/globe.jpeg'
    import lastSupperImage from '../assets/lastSupper.jpeg'
    import juliusImage from '../assets/juliusCaesar.jpeg'
    import purplePrincessImage from '../assets/purplePrincess.jpeg'
    import solidLifeImage from '../assets/solidLife.jpeg'


    export default {
        name: 'HomeView',

        data: function () {
            return {
                profileImg: profilePic,
                jmkImg: jmkImage,
                globeImg: globeImage,
                lastSupperImg: lastSupperImage,
                featuredShows: [
                    {
                        title: "The Solid Life Of Sugar Water",
                        company: "The Orange Tree Theatre",
                        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed in orci eu velit commodo cursus. Vestibulum vitae blandit magna. Aenean ac tincidunt nisl. Integer efficitur viverra turpis ac volutpat. Quisque at ipsum ut nisl tempor molestie. Aenean lobortis ipsum nec blandit iaculis. Nulla maximus iaculis lacus eget blandit. Donec lacus nisl.",
                        image: solidLifeImage,
                        imageAlt: "The Solid Life of Sugar Water promotional poster. View underwater a male and female tread water. We cannot see their faces",
                        imageCopyright: "John Smith"
                    },
                    {
                        title: "The Purple Princess",
                        company: "Guildford Shakespeare Company",
                        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed in orci eu velit commodo cursus. Vestibulum vitae blandit magna. Aenean ac tincidunt nisl. Integer efficitur viverra turpis ac volutpat. Quisque at ipsum ut nisl tempor molestie. Aenean lobortis ipsum nec blandit iaculis.",
                        image: purplePrincessImage,
                        imageAlt: "the audience at the globe theatre",
                        imageCopyright: "John Smith"
                    },
                    {
                        title: "Julius Caesar",
                        company: "Shakespeare's Globe",
                        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed in orci eu velit commodo cursus. Vestibulum vitae blandit magna. Aenean ac tincidunt nisl. Integer efficitur viverra turpis ac volutpat. Quisque at ipsum ut nisl tempor molestie. Aenean lobortis ipsum nec blandit iaculis. Nulla maximus iaculis lacus eget blandit. Donec lacus nisl, dignissim sed ullamcorper cursus, iaculis convallis sem. Nam varius odio et bibendum auctor. Duis ut efficitur felis.",
                        image: juliusImage,
                        imageAlt: "the audience at the globe theatre",
                        imageCopyright: "John Smith"
                    }
                ],
                contactForm: {
                    name: "",
                    email: "",
                    message: ""
                }
            }
        },

        methods: {
            scrollMeTo(refName) {
                const element = this.$refs[refName]
                const top = element.offsetTop - 100

                window.scrollTo(0, top)
            },

            handleSubmit() {
                console.log(this.contactForm)
            }
        }
    }
</script>

<style scoped>
    header {
        background: black;
        background-image: url(../assets/globe.jpeg);
        background-size: cover;
        max-height: 230px;
    }

    .btn-custom-primary {
        background: #ff7777;
        color: white;
    }

    .btn-custom-primary:hover,
    .btn-custom-primary:focus {
        background: #c85d5d !important;
        color: white !important;
    }

    .btn-custom-secondary {
        background: #00303b;
        color: white;
    }

    .btn-custom-secondary:hover,
    .btn-custom-secondary:focus {
        background: #015669 !important;
        color: white !important;
    }

    .profile-img {
        height: 250px;
        aspect-ratio: 1/1;
    }

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

    .surname {
        white-space: nowrap;
    }

    .jmk-jumbotron {
        background: rgba(0, 50, 61, 0.698);
        background-image: url(../assets/jmk.jpeg);
        background-size: cover;
        background-position: center;
        background-blend-mode: darken;
    }

    .about-img {
        overflow: hidden;
        object-fit: cover;
        width: 100%;
        height: 100%;
    }

    .featured-shows-wrapper {
        background: #fecf95;
    }

    .featured-show-card {
        border: 1px solid #00303b;
        box-shadow: 0px 1px 5px #00303b;
    }

    .featured-show-card-height {
        height: 100%;
    }

    .press-card {
        border-radius: 10px;
        border: 2px solid #00303b;
        box-shadow: 0px 1px 5px #00303b;
    }

    .press-text {
        text-align: left;
    }

    .footer-wrapper {
        background: #00303b;
    }

    .contact-form {
        max-width: 650px;
        margin: 0 auto;
    }

    .site-info {
        color: white;
        opacity: .5;
    }
</style>
