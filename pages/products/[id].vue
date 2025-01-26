<template>
    <div>
        <Head>
            <Title>PreamShop | {{ product.title }}</Title>
            <Meta name="description" :content=product.description />
        </Head>
        <div class="container">
            <img :src=product.thumbnail>
            <div class="detail">
                <h1>ชื่อสินค้า : {{product.title}} </h1>
                <h2>รายละเอียดสินค้า : {{ product.description }}</h2>
                <h2>หมวดหมู่ : {{ product.category }}</h2>
                <h2>ราคา : {{ product.price }}</h2>
            </div>
        </div>
    </div>
</template>

<script setup>
    const {id} = useRoute().params
    const {data: product} = await useFetch('https://dummyjson.com/products/'+id) //เอาข้อมูลมาจาก dummyjson หมวด products
    //console.log(product) //เอาไว้ดูรายละเอียดใน inspect
</script>

<style scoped>
.container{
    display: flex;
    justify-content: center;
}
.detail{
    padding-left: 10px;
}
</style>