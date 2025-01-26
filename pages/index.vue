<template>
    <div>
        <header>
            <nav>
                <h1 class="logo">Resume</h1>
                <NuxtLink to="/">หน้าแรก</NuxtLink>
                <NuxtLink to="/about">เกี่ยวกับเรา</NuxtLink>
                <NuxtLink to="products">สินค้าทั้งหมด</NuxtLink>
            </nav>
        </header>
        <h1>หน้าแรก index.vue</h1>
    </div>
</template>

<script setup>

</script>

<style scoped>
nav{
    margin: 10px auto;
    padding: 10px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #c58d8d;
}
nav a{
    color: white;
    text-decoration: none;
    margin-left: 12px;
    font-size: 18px;
    padding: 10px;
}
nav a:hover{
    color: aquamarine;
}
.logo{
    margin-right: auto;
    padding-left: 10px;
    color: white;
}
</style>