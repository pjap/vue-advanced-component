<template>
  <div>
    <h4>New Quote</h4>
    <button @click="counter++" class="btn btn-info">Increased!</button>
    <p>{{ counter }}</p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      counter: 0
    }
  },
  destroyed() {
    console.log('Destroyed Has Been Called!');
  },
  deactivated() {
    console.log('Components Was Deactivated!');
  },
  activated() {
    console.log('Components Was Activated!');
  }
}
</script>

<style scoped>
div {
  /* border: 1px solid #ccc; */
  box-shadow: 1px 1px 2px black;
  padding: 30px;
  margin: 30px auto;
  text-align: center;
}
h4 {
  color: green;
}
</style>
