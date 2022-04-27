<template>
    <div>
        <h1>About</h1>
    </div>
    <div id="flex-container">
        <div id="text-item">
            <p>
                Hi! My name is Brian Estiller and I love creating applications on the internet. My interest in web development started back in 2020 when the COVID pandemic started and I wanted to learn a skill that I could use while at home.
            </p>
            <p>
                Today, I'm interested in deploying machine learning models and REST APIs using technologies like Python, Docker and Amazon Web Services.
            </p>
            <p>
                Here are some technologies I've been working with:
            </p>
            <p>
                <ul>
                    <li>Python</li>
                    <li>Flask</li>
                    <li>Javascript</li>
                    <li>VueJS</li>
                    <li>Docker</li>
                    <li>AWS EC2</li>
                    <li>Route 53</li>
                    <li>CloudFront</li>
                </ul>
            </p>
        </div>
        <div id="img-item">
            <img :src="require('@/assets/pfp.png')" alt="">
        </div>
    </div>

</template>

<script setup>

</script>

<style scoped>
#flex-container {
    display: flex;
    justify-content: center;
    align-items: flex-start;
}

#text-item {
    width: clamp(200px, 100%, 750px);
    font-size: clamp(1.25em, 1.25vw, 1.5em);
}

h1 {
    margin: 0;
    padding: 0;
    font-size: 3em
}

ul {
    display: grid;
    grid-template-columns: auto auto;
    color: white;
}

img {
    -webkit-filter: grayscale(60%);
    filter: grayscale(60%);
    transition: filter 0.4s;
    transition: -webkit-filter 0.4s;
}

img:hover {
    -webkit-filter: grayscale(0%);
    filter: grayscale(0%);
}

@media screen and (min-width: 721px) {
    #img-item {

    display: flex;
    justify-content: center;
    align-items: center;
}

    img {
        width: 80%;
        height: 80%;


    }
}

@media screen and (max-width: 720px) {
    #img-item {
    display: none;
    }
}


</style>