<script setup>
import Resume from '../components/resume.vue'
</script>

<template>
    <section class="starter">
        <img class='check 'src='../../public/GlitchyText.svg' alt="idk">
        <audio controls>
        <source src="../../public/2024WebDevaudio.mp3">
        </audio>
        <Resume/>
    </section>
</template>

<style scoped>
    .starter {
        border: 2px solid black;
        padding: 5px;
        border-radius: 10px;
        background-color: black;
        height: 500px;
        width: 900px;
    }
</style>