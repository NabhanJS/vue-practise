<template>
    <div>
        <ul>
            <li v-for="product in products" :key="product">
                {{ product.productStock }}

            </li>
        </ul>
        
    </div>

  
</template>

<script>
export default {
    props: ['products']

}
</script>

<style>

</style>