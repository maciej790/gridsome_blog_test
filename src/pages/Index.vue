<template>
  <Layout>
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

    <h1>Hello, world!</h1>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur
      excepturi labore tempore expedita, et iste tenetur suscipit explicabo!
      Dolores, aperiam non officia eos quod asperiores
    </p>

    <p class="home-links">
      <a href="https://gridsome.org/docs/" target="_blank" rel="noopener"
        >Gridsome Docs</a
      >
      <a
        href="https://github.com/gridsome/gridsome"
        target="_blank"
        rel="noopener"
        >GitHub</a
      >
    </p>

    <div class="blog">
      <div
        class="blog_article"
        v-for="edge in $page.posts.edges"
        :key="edge.node.id"
      >
        <h2>{{ edge.node.title }}</h2>
        <g-image v-if="edge.node.image" :src="edge.node.image" class="x" />
      </div>
    </div>
  </Layout>
</template>

<page-query>
 query {
    posts: allPost {
      edges {
        node {
          id
          title
          image
        }
      }
    }
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: "Hello, world!",
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}

.blog {
  width: 100%;
  margin: 100px 0 0 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.blog_article {
  width: 80%;
  height: 100px;
  background: rgb(68, 225, 68);
  margin: 20px 0 20px 0;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
}

.x {
  width: 100px;
  height: 100px;
}
</style>
