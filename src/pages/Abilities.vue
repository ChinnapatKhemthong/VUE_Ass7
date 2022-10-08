<template>
    <div>
      <Navbar />
      
      <h1 class="heading"> MY <span>Skills</span> </h1>
      <!---article-->
      <main class="content margin-auto">
        <article class="artical">
          <section class="text-center title">
            <h1>{{artical}} </h1>
          </section>
  
          <section class="row-50 bg-white left">
            <table class="table-cute">
              <tr>
            <h1><td>{{ sub_article }}</td></h1>
                <!--Emoji Windows: WIN+. or WIN+; | MAC: ^+Command+space-->
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article1 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article2 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article3 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
            </table>
          </section>
          <section class="row-50 bg-red left">
            <table class="table-cute">
              <tr>
                <h1><td>{{ sub_article4 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article5 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article6 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
              <tr>
            <h1><td>{{ sub_article7 }}</td></h1>
                <td>⭐⭐⭐⭐⭐</td>
              </tr>
            </table>
          </section>
        </article>
      </main>
    </div>
  </template>
  
  <script>
  import Navbar from "../components/Navbar.vue";
  import axios from "axios";
  //https://634148bf20f1f9d7996fc7e1.mockapi.io/profile/v1/chinnapatbom
  export default {
    components: { Navbar },
    methods: {
      async fetchAbilities() {
        try {
          let res = await axios.get(
            "https://634148bf20f1f9d7996fc7e1.mockapi.io/profile/v1/chinnapatbom"
          );
          this.fetchAbilities = res.data;
        } catch (error) {}
      },
    },
    data() {
      return {
        
        sub_article: "Cooking",
        sub_article1: "Gaming",
        sub_article2: "Sports",
        sub_article3: "Photography",
        sub_article4: "Drawing",
        sub_article5: "Sleeping",
        sub_article6: "Reading",
        sub_article7: "Chilling",
      };
    },
    beforeMount() {
      this.fetchAbilities();
    },
  };
  </script>
  
  <style>
  </style>