<template>
    <div>
        <header class='site-navbar'>
            <ul>
                <nuxt-link to="/"><li>Home</li></nuxt-link>
                <nuxt-link to="/jokes"><li>Jokes</li></nuxt-link>
                <nuxt-link to="/about"><li>About</li></nuxt-link>
            </ul>
        </header>
    </div>
</template>

<script>
export default {

}
</script>

<style>
*{
    margin:0;
    font-size: 20px;
    box-sizing: border-box;
}

h1,h2,h3,h4,h5,h6,p{
max-width:920px;
padding-left: 200px;
padding-right: 200px;
}

.site-navbar{
    padding:10px;
    background:black;
}
.site-navbar ul{
    list-style: none;
    display: flex;
}

.site-navbar ul li {
    margin-right:40px;
    color:white;
}

.site-navbar ul a{
    text-decoration: none;
}

.site-navbar ul li:hover{
    color: lightgreen;
    transition:ease-in-out 0.4s;
}

</style>
