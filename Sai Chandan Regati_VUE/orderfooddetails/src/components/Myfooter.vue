<!-- eslint-disable vue/multi-word-component-names -->

<template>
  <div class="footer">
    <p><i>{{ quote }}. By Ordering from your favourite Restaurant.</i></p>
  </div>
</template>

<script>
export default {
  props: {
    quote: {
      type: String,
      required: true,
    },
  },
};
</script>

<style >

.footer {
  background-color: #ff0000;
  color: #fff;
  padding: 10px;
  text-align: center;
  font-size: large;
}
</style>


