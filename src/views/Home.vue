<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from "../components/PostList";
import { ref } from "vue";

export default {
  name: "Home",
  components: { PostList },
  setup() {
    const posts = ref([
      {
        title: "welcome to the blog",
        body:
          "  Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus cum, esse repudiandae odio ducimus sed aliquid quo hic at corrupti eveniet id delectus architecto dolorum earum repellat atque expedita odit rem. Dolor iure necessitatibus reprehenderit aut pariatur distinctio, dolorum, fugit tempore optio minus totam atque qui magni commodi a animi dignissimos deserunt. Quidem iure animi veniam reiciendis debitis in adipisci, delectus at ipsum, quam quisquam incidunt nemo. Dolorem obcaecati iste ullam dolores neque consequuntur, voluptatem libero tempora atque molestias qui, exercitationem iure? Blanditiis error excepturi quo culpa praesentium numquam animi sed consequatur maiores. Culpa quod maiores corporis, quo totam fugiat possimus ea saepe consequuntur cum soluta reiciendis illum dolores maxime odio debitis, excepturi incidunt tempore. Praesentium architecto eaque voluptatum fugit incidunt quaerat asperiores harum cumque saepe, tenetur nam numquam sed doloremque sequi ad exercitationem? Ducimus ea ad pariatur voluptates labore voluptatibus delectus dicta sed possimus consectetur, similique sit minima accusantium repellat distinctio, officiis voluptatem animi quos praesentium magnam. Dolores, sit quidem eaque omnis nulla ullam enim modi possimus voluptatibus deserunt odit. Commodi architecto adipisci ut veniam earum repellendus corporis similique iste, temporibus, neque eaque saepe distinctio. Repellat corporis mollitia commodi quisquam rem quae voluptatum dolorum, consequuntur, molestiae, eius ipsam ipsum aperiam est architecto maxime nihil dolore! Sequi voluptates iusto architecto mollitia consequatur dicta veniam, quae quisquam, nisi quia quis porro laboriosam quos. Ad perferendis veritatis nobis molestiae maxime iusto temporibus assumenda quas, hic dolore quo quisquam magnam voluptate distinctio enim quos optio vero saepe similique? Rem ipsam quisquam cum officiis voluptatem labore minima, accusamus veniam ut temporibus soluta ipsa consectetur nostrum quibusdam deserunt nulla vitae excepturi nihil sint? Expedita possimus accusantium ex, facilis placeat quia aperiam harum quidem voluptatem, repudiandae id repellendus non deleniti modi, adipisci rerum magnam iusto quam ducimus ullam soluta assumenda tenetur? Quis iste vero ab quasi maiores distinctio. Ipsum atque quod commodi, ut dolor aut id exercitationem quia quaerat iure impedit laboriosam illo aliquid eius beatae autem cumque non officiis reprehenderit minima? Delectus beatae natus voluptates, minus doloribus commodi dolor dolores? Totam dolor suscipit laborum atque explicabo vitae commodi, animi dolores similique, maiores ut nisi. Minima voluptates et, quisquam vel doloribus natus veritatis vitae, omnis libero praesentium nam ducimus assumenda, dicta veniam perferendis ipsam. Iure suscipit accusamus voluptatem fugit iste ut deleniti fuga odit, aut tenetur distinctio deserunt placeat at cumque repellendus, delectus fugiat repudiandae quibusdam error enim itaque a architecto. Excepturi accusantium dolores a reiciendis molestiae! Placeat praesentium ab, facere cupiditate magni maiores rerum? Eius voluptatum ut eveniet tempora rem assumenda libero nesciunt possimus laborum optio pariatur accusantium, ullam qui temporibus quidem maiores amet odit sit dolores repudiandae officia perferendis voluptas iste. Nesciunt nam officia ducimus mollitia inventore voluptatibus, similique, nemo esse nisi impedit quisquam illum expedita voluptatum! Repellat unde harum, soluta explicabo quidem eum quod amet numquam deleniti culpa vero et non voluptatum cupiditate ea omnis odit sapiente recusandae earum qui quis voluptas laborum ullam nemo. Id ex quidem voluptate dolores, nisi aliquid laboriosam exercitationem debitis incidunt. Asperiores, sit unde quas esse maxime repellendus",
        id: 1,
      },
      { title: "top 5 CSS tips", body: "Lorem ipsum", id: 2 },
    ]);

    return { posts };
  },
};
</script>

<style></style>
