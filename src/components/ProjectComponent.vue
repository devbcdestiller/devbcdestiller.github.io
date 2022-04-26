<template>
    <div>
        <h1>Projects</h1>
    </div>
    <div id="project-container">
        <div class="item-container" v-for="content in contents" :key="content.id">
            <ProjectItems :items="content" />
        </div>
    </div>
</template>

<script setup>
import ProjectItems from './items/ProjectItems.vue'

const contents = [
    {
        id: 0,
        a: 'https://github.com/devbcdestiller/whats-cat-api',
        title: "What's Cat API",
        body: "Cat breed classifier using Inceptionv3. Deployed using Tensorflow Serving and Flask, built with Docker Compose.",
        image: "proj1.png",
        tech: [
            {
                id: 0,
                item: "EC2"
            },
            {
                id: 1,
                item: "Tensorflow"
            },
            {
                id: 2,
                item: "RESTful API"
            },
            {
                id: 3,
                item: "Python"
            }
        ]
    },
    {
        id: 1,
        a: 'http://spam-detekt.herokuapp.com/',
        title: "Spam Detection API",
        body: "Spam classifier using LSTM-Recurrent Neural Networks. Deployed using Tensorflow Serving and Flask, built with Docker Compose.",
        image: "proj2.png",
        tech: [
            {
                id: 0,
                item: "EC2"
            },
            {
                id: 1,
                item: "Tensorflow"
            },
            {
                id: 2,
                item: "RESTful API"
            },
            {
                id: 3,
                item: "Python"
            }
        ]
    }
    
];
</script>

<style>
.item-container {
    margin-bottom: 12.5vh;
    
}

.item-container:nth-of-type(odd) {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: right;
}

.item-container:nth-of-type(odd) .text-container {
    transform: translateX(-2vw);
}

.item-container:nth-of-type(even) {
    display: flex;
    flex-direction: row-reverse;
    justify-content: center;
    align-items: center;
}

.item-container:nth-of-type(even) .text-container {
    transform: translateX(2vw);
}

h1 {
    margin: 3vh 0;
    padding: 0;
    font-size: 2em
}
</style>