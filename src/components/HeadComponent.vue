<template>
    <div id="container">
        <div class="items">
            <h1>Brian Estiller</h1>
        </div>
        <div class="items">
            <h2>I love building web apps.</h2>
        </div>
        <div class="items">
            <p id="flavor-text">
                I'm a software developer specialized in building web applications specifically in the back-end/server-side (occasionally on the front-end). I build and deploy REST APIs with technologies like Python, Docker and AWS.
            </p>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
@keyframes fadeInDown {
    from {transform: translate(0, 50px);}
    to {transform: translate(0, 0)}
}

#container {
    animation: fadeInDown 1.75s 1;
}
.items {
    margin: 0;
    padding: 0;
}

#flavor-text {
    width: clamp(200px, 70%, 750px);
    font-size: clamp(1.25em, 1.25vw, 1.5em);
}

h1 {
    font-size: clamp(3.5em, 4.15vw, 5em);
    margin: 0;

}

h2 {
    font-size: clamp(3em, 4vw, 4.5em);
    margin: 0;
    padding: 0;
}
</style>
