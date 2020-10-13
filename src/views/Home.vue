<template>
    <div class="home">
        <main >
            <img alt="Our first table" src="@/assets/table.jpg">
            <img id="project2" alt="Our second table" src="@/assets/table2.jpg">
            <img alt="Our third table" src="@/assets/table3.jpg">
        </main>

        <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    </div>
</template>

<script>
    // @ is an alias to /src
    //import HelloWorld from '@/components/HelloWorld.vue'

    export default {
        name: 'Home',
        components: {
            //HelloWorld
        }
    }
</script>
<style>
    img {
        width: 100%;
        height: 95%;
    }
</style>
