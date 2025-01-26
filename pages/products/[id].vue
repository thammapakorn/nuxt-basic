<template>
    <div>
        <div class="container">
            <img :src=prodouct.thumbnail>
            <div class="detail">
                <h1>ชื่อสินค้า : {{prodouct.title}} </h1>
                <h2>รายละเอียดสินค้า : {{ prodouct.description }}</h2>
                <h2>หมวดหมู่ : {{ prodouct.category }}</h2>
                <h2>ราคา : {{ prodouct.price }}</h2>
            </div>
        </div>
    </div>
</template>

<script setup>
    const {id} = useRoute().params
    const {data: prodouct} = await useFetch('https://dummyjson.com/products/'+id) //เอาข้อมูลมาจาก dummyjson หมวด products
    //console.log(prodouct) //เอาไว้ดูรายละเอียดใน inspect
</script>

<style scoped>

</style>