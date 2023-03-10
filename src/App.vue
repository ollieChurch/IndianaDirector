<template>
    <div id="app">
        <router-view />
    </div>
</template>

<style>
    .debug {
        outline: 2px solid red;
    }

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        overflow-x: clip;
    }

    .sr-only {
        display: none !important;
    }

    .btn-custom-primary {
        background: #ff7777 !important;
        color: white !important;
    }

    .btn-custom-primary:hover,
    .btn-custom-primary:focus {
        background: #c85d5d !important;
        color: white !important;
    }

    .btn-custom-secondary {
        background: #00303b !important;
        color: white !important;
    }

    .btn-custom-secondary:hover,
    .btn-custom-secondary:focus {
        background: #015669 !important;
        color: white !important;
    }
</style>
