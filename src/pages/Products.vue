<template>
  <Layout>
    <h1>Welcome to Products site!</h1>
    <div class="products">
      <div
        class="product"
        v-for="edge in $page.products.edges"
        :key="edge.node.id"
      >
        <h2>{{ edge.node.title }}</h2>
      </div>
    </div>
  </Layout>
</template>

<page-query>
  query {
    products: allProduct{
      edges{
        node{
          id
          title
        }
      }
    }
  }
</page-query>

<style>
.products {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.product {
  width: 100%;
  text-align: center;
  margin: 30px 0 30px 0;
  background: rgb(246, 181, 60);
  color: white;
}
</style>
