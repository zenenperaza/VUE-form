<template>
    <div class="container">
        <PostDetail v-for="elm in info" :key="elm.title" :title="elm.title" :content="elm.content"/>
    </div>
</template>

<script lang="ts" setup>
   import PostDetail from './PostDetail.vue';

   interface Post{
    title: string,
    content: string
   }

   let info:Array<Post> = [
    {
        title: "Este es el post 1",
        content: "texto de ejemplo 1"
    },
    {
        title: "Este es el post 2",
        content: "texto de ejemplo 2"
    },
    {
        title: "Este es el post 3",
        content: "texto de ejemplo 3"
    },
    {
        title: "Este es el post 4",
        content: "texto de ejemplo 4"
    },
    {
        title: "Este es el post 5",
        content: "texto de ejemplo 5"
    },
   ]
</script>

<style scoped>
.container{
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-around;
}
</style>