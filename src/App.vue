<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button class="btn btn-primary" @click="selectedComponent='appQuote'">Quote</button>
        <button class="btn btn-success" @click="selectedComponent='appAuthor'">Author</button>
        <button class="btn btn-info" @click="selectedComponent='appNew'">New</button>
        <hr>
        <p>{{selectedComponent}}</p>
        <keep-alive>
        <component :is="selectedComponent">
          <p>Defualt componet</p>
        </component>
        </keep-alive>
        <!-- <app-quote>
          <h2 slot="title">{{quoteTitle}}</h2>
          <p>A Wonderful Quote</p>
        </app-quote>
        <hr>
        <app-author></app-author> -->
      </div>
    </div>
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";
import New from "./components/New.vue";
import Author from "./components/Author.vue";
export default {
  data: function() {
    return { quoteTitle: "The Quote", selectedComponent: "appQuote" };
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  }
};
</script>

<style>
</style>
