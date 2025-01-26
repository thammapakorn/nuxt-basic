<template>
    <div>
        <div v-for="product in data.products">
            <NuxtLink :to="`/products/${product.id}`">
                <h2>{{ product.title }}</h2>
            </NuxtLink>
            <img :src=product.thumbnail>
        </div>
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