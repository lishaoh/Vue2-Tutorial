<template>
<div class="container">
  <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="row">
        <div class="col-sm-12 text-center">
            <dir class="alert alert-info">Info: Click on a Quote to delete it !</dir>
        </div>
    </div>
</div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import Header from "./components/Header";

export default {
  data: function() {
    return {
      quotes: ["This is lishaohua's Mac"],
      maxQuotes: 10
    };
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("Please delete a Quote first !");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header
  }
};
</script>

<style>
div.component {
  border: 1px solid black;
  padding: 30px;
}
</style>
