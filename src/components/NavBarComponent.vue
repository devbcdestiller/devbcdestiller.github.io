<template>
    <ul id="navbar-container">
        <div>
            <li>
                <a id="home" href="" target="_self">BE</a>
            </li>
        </div>
        <div>
            <li>
                <a href="#head-section">Home</a>
            </li>
            <li>
                <a href="#about-section">About</a>
            </li>
            <li>
                <a href="#works-section">Works</a>
            </li>
            <li>
                <a href="#contact-section">Contact</a>
            </li>
        </div>
    </ul>
</template>

<style scoped>
#navbar-container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
}

#navbar-container li {
    float: left;
    display: block;
    text-align: center;
    padding: 2vw;
}

#home {
    font-weight: bold;
    font-size: 1.5em;
}
a {
    padding: 0;
    margin: 0;
    font-size: 1.15em;
}



</style>