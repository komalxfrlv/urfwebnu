<template>
    <section class="products">
        <h1>Наша продукция</h1>
        <div class="container">
            <ProductsListComponent></ProductsListComponent>
        </div>
    </section>
</template>
<style lang="scss" scoped>
.products {
    h1 {
        margin-top: 90px;
        margin-bottom: 80px;
        text-align: center;
        font-weight: 300;
    }

    h2 {
        text-align: center;
        font-weight: 300;
        margin-bottom: 40px;
    }

    .container {
        margin-bottom: 90px;
    }
}
</style>