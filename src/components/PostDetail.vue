<template>
<div class="post"> 
    <h3>{{ props.title }}</h3>
    <p>{{ props.content }}</p>

</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
    name: 'PostDetail',
    props: {
        title:{
            type: String,
            required: true
        },
        content : {
            type: String,
            requiered: false,
            default: "Post sin contenido"
        }
    },
    setup(props){
        return {props}
    }
})
   
</script>

<style scoped>
.post{
    width: 300px;
    height: 200px;
    border-radius: 10px;
    background-color: antiquewhite;
    margin: 10px;
    padding: 10px;


}
</style>