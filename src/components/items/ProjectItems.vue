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
                <h2>{{ props.items.title }}</h2>
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
.img-item {
    background-color: #353535;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: -2;
}

.text-container {
    width: 50%;
    z-index: -1;
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
