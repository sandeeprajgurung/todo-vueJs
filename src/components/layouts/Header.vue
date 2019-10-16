<template>
    <header class="header">
        <h1>Todo List</h1>
        <div id="nav">
            <router-link to="/" class="link">Home</router-link> |
            <router-link to="/about" class="link">About</router-link>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    .header{
        background: #578bc1;
        color: aliceblue;
    }
    .header h1 {
        padding-top: 20px;
    }
</style>