<template>
  <Layout class="container">
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <div class="top-container">
      <h1>
        Git Workshop 2022 <br />
        Powered by IEEE IHU Thess Student Branch
      </h1>
      <!-- <g-image alt="Example image" src="~/assets/ieee.png" width="335" /> -->
    </div>

    <p class="description">
      These are the people that participated and contributed to our 2022 Git
      Workshop
    </p>

    <div class="cards">
      <contributor-card
        v-for="edge in $page.contributors.edges"
        :key="edge.node.id"
        :contributor="edge.node.content"
      >
      </contributor-card>
    </div>

    <p class="home-links">
      <a href="https://ieeeihuthess.org" target="_blank" rel="noopener"
        >Our Website</a
      >
      <a href="https://github.com/ieee-ihuthess" target="_blank" rel="noopener"
        >GitHub</a
      >

      <a
        href="https://www.facebook.com/ieee.ihuthess/"
        target="_blank"
        rel="noopener"
        >Facebook</a
      >

      <a
        href="https://www.instagram.com/ieee.ihuthess/"
        target="_blank"
        rel="noopener"
        >Instagram</a
      >
    </p>
  </Layout>
</template>

<page-query> 
query { contributors: allContributor { edges { node { content } } } }
</page-query>

<script>
import ContributorCard from "../components/ContributorCard.vue";
export default {
  components: { ContributorCard },
  metaInfo: {
    title: "Git Workshop 2022",
  },
};
</script>

<style>
* {
  font-family: Jura !important;
  color: white;
}

h1 {
  font-size: 2em;
}

.home-links {
  margin-top: 25px;
}

.home-links a {
  margin-right: 1rem;
  color: white;
}

.top-container {
  display: flex;
  padding: 20px 5px;
  justify-content: center;
  align-items: center;
  border-bottom: 1px solid;
}

.container {
  text-align: center;
}

.description {
  margin-top: 20px;
  font-size: 1.3em;
}

.cards {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
}

.cards div {
  margin-top: 15px;
}
</style>
