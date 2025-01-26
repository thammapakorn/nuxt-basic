<template>
    <div>
        <h1>สินค้าทั้งหมดในเว็บไซต์</h1>
        <ul v-for="product in data.products">
            <li>{{ product.title }}</li>
        </ul>
    </div>
</template>

<script setup>
useHead({
    title:"สินค้าทั้งหมด",
    meta:[
        { name:"description",content:"ร้านค้าขายคีย์บอร์ด" }
    ]
})
const {data: data} = await useFetch('https://dummyjson.com/products?limit=10') //เอาข้อมูลมาจาก dummyjson หมวด products
console.log(data)
</script>

<style scoped>

</style>