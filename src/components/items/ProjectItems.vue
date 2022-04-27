<template>
    <div class="img-item">
        <a :href="props.items.a" target="_blank">
            <img :src="require('@/assets/' + props.items.image)" alt="">
        </a>
    </div>
    <div class="text-container">
        <div class="text-item">
            <div>
                <h3>Personal Project</h3>
                <h2><a :href="props.items.a" target="_blank">{{ props.items.title }}</a></h2>
            </div>
            <div class="body-wrapper">
                <p>
                    {{ props.items.body }}
                </p>
            </div>
            <div class="tech-container">
                <p v-for="item in props.items.tech" :key="item.id">{{ item.item }}</p>
            </div>
        </div>
    </div>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
    items: Object
})

console.log(props.items)

</script>

<style scoped>
@keyframes fadeToNormal {
    from {
        -webkit-filter: grayscale(60%);
        filter: grayscale(60%);
        width: 30vw;
    }
    to {
        -webkit-filter: grayscale(0%);
        filter: grayscale(0%);
        width: 31vw;
    }
}

.img-item {
    background-color: #353535;
    display: flex;
    justify-content: center;
    align-items: center;

}

.text-container {
    width: 50%;

}

.body-wrapper {
    background-color: #ededed;
    padding: 1em;
    margin: 0;
}

.body-wrapper p{
    color: #353535;

}

.tech-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    font-size: 0.75em;
}

img{
    aspect-ratio: 16/9;
    margin: 0;
    padding: 0;
    width: 30vw;
    height: auto;
    -webkit-filter: grayscale(80%);
    filter: grayscale(80%);
    transition: -webkit-filter 1s;
    transition: filter 1s;
    transition: width 0.3s;
}

img:hover {
    -webkit-filter: grayscale(0%);
    filter: grayscale(0%);
    width: 31vw;
}
a {
    color: white;
    transition: color 0.2s;
}

a:hover {
    color: #202020;
}
h2 {
    color: white;
    margin: 0;
    padding: 0;
    font-size: 1.25em
}

h3 {
    font-weight: normal;
    color: #b4b4b4;
    margin: 0;
    padding: 0;
    font-size: 1em
}

</style>
