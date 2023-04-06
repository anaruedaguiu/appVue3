<script>
export default {
    data(){
        return{
            title: "This is my title for Monday",
            person:{
                id: 1,
                name : 'Bill',
                img : "http://www.buscabiografias.com/img/people/Bill_Murray.jpg",
            },
            msg: "Bill uno de los integrantes de los cazafantasmas",
        }
    },
};
</script>


<template>
    <h3>{{ title }}</h3>
    <div :id="person.id"> 
        <h4>{{ person.name }}</h4>
        <img :src="person.img" :alt="person.name">
    </div>
    <h5 v-html="msg"></h5>
</template>


<style lang="css" scoped>
h3 {
    color:magenta;
}
</style>