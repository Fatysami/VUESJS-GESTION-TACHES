<template>
    <header>
        <h1>{{ title }}</h1>
        <Button text="Add task" color="green"/>
    </header>
</template>
<script>
import Button from './Button'
export default {
    name:'AppHeader',
    props:{
        title: String,
    },
    components:{
        Button
    }
}
</script>
<style scoped>
Header {
display: flex;
justify-content: space-between;
align-items: center;
margin-bottom:20px ;
}

</style>