<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <br>
        <button class="btn btn-warning" @click="componentSelector = 'appQuote'">Quote</button>
        <button class="btn btn-info" @click="componentSelector = 'appAuthor'">Author</button>
        <button class="btn btn-success" @click="componentSelector = 'appNew'">New Quote</button>
        <span> You Are Here --> <strong>{{ componentSelector }}</strong></span>
        <!-- Make Sure For The Component Keep Alive and No Destroy/Re Render All The Data -->
        <keep-alive>
          <component :is="componentSelector">
            <h2 slot="title">{{ quoteTitle }}</h2>
            <p>Default Content</p>
          </component>
        </keep-alive>
        <!-- If Using Slot All The Parent Data Will Render In Child Except Style -->
        <!-- <appQuote>
          <h2 slot="title">{{ quoteTitle }}</h2>
          <p slot>A Wonderful Quote</p>
        </appQuote> -->
      </div>
    </div>
  </div>
</template>

<script>
import Quote from './components/Quote.vue'
import Author from './components/Author.vue'
import Newcomp from './components/New.vue'

export default {
  data: function() {
    return {
      quoteTitle: 'The Quote',
      componentSelector: 'appQuote'
    }
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: Newcomp
  }
}
</script>

<style scoped>
</style>
