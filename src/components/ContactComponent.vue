<template>
    <div id="text-container">
        <div>
            <h1>Contact</h1>
        </div>
        <div>
            <p>
                You can contact me by email. My mailbox is always open, and I will respond via those channels.
            </p>
        </div>
        <div>
            <a href="mailto: dev.bcdestiller@gmail.com">
                <p id="email">dev.bcdestiller@gmail.com</p>
            </a>
        </div>
    </div>
</template>

<style scoped>
#text-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;

}

#email {
    text-align: center;
    margin: 2vw;
    padding: 2vh 2vw;
    border: 2px solid white;
    color: white;
    transition: border 0.3s;

}

#email:hover {
    border: 5px solid #202020;
}

h1 {
    margin: 0;
    padding: 0;
    font-size: 3em
}

p {
    font-size: clamp(1.25em, 1.25vw, 1.5em);
    margin: 2.5vh 0;
}
</style>