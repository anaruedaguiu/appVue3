<script>
import ChildComponent from './ChildComponent.vue'
export default {
    components: { ChildComponent },
        data() {
            return {
                movieTitle: 'Superman',
                brandParent :"",
                count : 0,
            }
        },
        methods: {
        receivedBrand(data){
            this.$brand = data;
            this.count++;
        }
    },
}
</script>

<template>
    <h2>I'm your Father</h2>
    <span>{{ movieTitle }}</span>
    <ChildComponent :movieTitle="movieTitle" @changeBrand="receivedBrand"></ChildComponent>
    <span>BRAND : {{ brand }} / {{ count }}</span>
</template>

<style>

</style>