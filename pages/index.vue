<template>
  <div class="container">
    <Hero >
      <div slot="header">
        <p>Soy el slot desde el padre index.vue Hero component</p>
      </div>
    </Hero>
    <section class="section">
      <RestaurantCard
        name= "Restaurant Mr Pacus."
        description= "Restaurant description"
        category= "burger"
        slug="restaurant-name"
        v-bind:likes="likes"
        v-on:onLikeButton="updateLikes"
      />
    </section>
  </div>
</template>

<script>
import RestaurantCard from "~/components/RestaurantCard";
import Hero from "~/components/Hero";
export default {
  components: {
    RestaurantCard,
    Hero
  },
  data: () => ({
    likes:0
  }),
  methods: {
    updateLikes () {
      this.likes++;
    }
  }
}
</script>
<style></style>
