<template>
    <header>
        <h1>{{title}}</h1>
        <Button @toggle-add-task="$emit('toggle-add-task')" text="Add Task" color="green"/> <!--Capital B as it's component not just button tag-->
    </header>
</template>

<!-- Array Form
<script>
    export default {
        name: 'Header',
        props: ['title'],   
    }
</script>
-->

<!-- Object form-->
<script>
    import Button from './Button' //Same folder so ./

    export default {
        name: 'Header',
        props: {
            title: String,
        },
        components:{
            Button
        },   
        methods: {
            onClick() {
                console.log('click')
            }
        }
    }
</script>

<style scoped>
    header{
        display:flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>