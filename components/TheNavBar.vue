<template>
    <nav class="nav">
        <div class="logo">
            <!-- <a href="" class="logo-text-lg">Nuxt Fundmentals</a> -->
            <nuxt-link :to="{name:'index'}" class="logo text-lg">HOME</nuxt-link>
            <!-- <span class="subheader"></span> -->
        </div>
    </nav>
</template>
<script>
export default {
    
}
</script>
<style scoped>

    .nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 10px;
        font-weight: lighter;
        letter-spacing: 0.5px;
    }

    .nav .logo{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .nav .logo .subheader{
        opacity: 0.70;
        flex-direction: column;
        justify-content: center;

}

    .nav .nav-contnet{
        font-size: 1rem;

    }


    .nav-contnet ul {
        display: flex;
        list-style: none;
    }
    .nav-contnet ul li{
        padding: 2px 10px;
    }

    .nav-contnet ul li:not(:first-of-type){
        border-left: 1px solid rgb(255,255,255,0.2);
    }
</style>