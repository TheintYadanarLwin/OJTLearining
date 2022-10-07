<template>
    <div class="container">
        <article>
            <h1 class="title">{{post.title}}</h1>
            <p>{{post.content}}</p>
            <span>Continue Learning with Documentation   =>   </span>
            <a :href="post.documentation" class="button-green" target="blank">Documentation</a>

        </article>

        <aside>
            <h3>What I'm learning</h3>
            <ul>
                <li v-for="related in relatedPosts">
                    <!-- <a :href="`/posts/${related.id}`">{{related.title}}</a> -->
                    <nuxt-link :to="`/posts/${related.id}`">{{related.title}}</nuxt-link>
                     <!-- <nuxt-link :to="post.related.id">{{related.title}}</nuxt-link> -->
                   
                </li>
            </ul>
        </aside>
    </div>
</template>
<script>
export default {
    data(){
        return{
    id: this.$route.params.id,
    
    posts:[
        {
            id:'NuxtJS',
            title:'What is Nuxt JS?',
            content:'Nuxt Js is an open source framework making web development simple and powerful.',
            documentation:'https://nuxtjs.org/'
   
        
        },
        {
            id:'VueJS',
            title:'What is Vue JS?',
            content:'Vue Js is the Progressive JavaScript Framework · ',
            documentation:'https://vuejs.org/guide/introduction.html'
        },
        {
            id:'Vuex',
            title:'What is Vuex',
            content:'Vuex is Vuex is a state management pattern + library for Vue.js applications. It serves as a centralized store for all the components in an application, with rules ensuring that the state can only be mutated in a predictable fashion.',
            documentation:'https://vuex.vuejs.org/guide/'
        },
        {
            id:'Laravel',
            title:'What is Laravel?',
            content:'Laravel is best described as a PHP framework used for programming web applications. It’s an open-source framework and is free to use. The applications built using Laravel use the MVC (model view controller) pattern, which refers to a particular architecture used to structure a web application.',
            documentation:'https://laravel.com/docs/9.x/readme'
       
        }

    ]
        }
    },
    computed:{
        post(){
            return this.posts.find(post => post.id === this.id)
        },
        relatedPosts(){
            return this.posts.filter(post => post.id !== this.id)
        }
    }
   
}
</script>
<style scoped>
.container{
    display: flex;
    justify-content: space-between;
    line-height: 1.5;
    margin-top: 100px;
}

article *{
    margin-bottom: 1rem;
    
}
span{
    font-size: smaller;
    color:darkorange;
}
aside{
    min-width: 280px;
    max-width: 280px;
    padding-left: 2rem;
}
.title{
    font-size: 2rem;
}
</style>