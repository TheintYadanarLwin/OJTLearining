<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        OJT LEARNING
      </h1>
      <h2 class="substitle">
        
      </h2>

      <div class="links">
        <!-- <a href="https://nuxtjs.org" 
        target="_blank" 
        class="button-green">Documentation </a> -->

         <nuxt-link :to="`/posts/NuxtJS`" class="button-green" target="blank">Get Started</nuxt-link>

        <a href="https://github.com/TheintYadanarLwin" 
        target="_blank"
        class="button-grey">My GitHub</a>

      </div>
    </div>
  </section>
</template>

<script>
  import Logo from '../components/Logo.vue';
export default {
  components:{
    Logo
  }
}
</script>

<style scoped>
  .container{
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;

  }

  .title{
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    letter-spacing: 1px;
  } 

  .substitle{
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
  }

  .links{
    padding-top: 15px;
   
  }
 
/* .button-green,
.button-grey{
    display: inline-block;
    border-radius: 4px;
    border: 1px solid #3b8870;
} */
  

</style>
