<template>
  <div>
    <div class="title">
      <!-- Using Slot For Pass Argument HTML From Outside To Child Components -->
      <slot name="title"></slot>
      <span style="color:black;font-size:12px;"><slot name="subtitle">The Subtitle In Here</slot></span>
    </div>
    <hr>
    <div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
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
  h2 {
    color: tomato;
  }
  .title {
    font-style: italic;
    text-transform: uppercase;
  }
</style>
