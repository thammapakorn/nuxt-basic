<template>
    <div class="container">
            <Head>
                <Title>PreamShop | หน้าแรกของเว็บไซต์</Title>
                <Meta name="description" :content="หน้าแรกของเว็บไซต์" />
            </Head>
            <h1>หน้าแรก index.vue</h1>
            <img src="/image/shopping.svg">
    </div>
</template>

<script setup>
useHead({
    title:"PreamShop | Homepage",
    meta:[
        {name:"description",content:"ร้านค้าขายคีย์บอร์ด"}
    ]
})
</script>

<style scoped>
.container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
img{
    width: 400px;
    height: 400px;
    
}
</style>