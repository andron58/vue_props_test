<template>
  <div class="hello">
    <template v-for="(item, index) in localArray">
      <input type="text" v-model="item.value" :key="`some_${index}`" />
    </template>
    <pre>
      {{ this.localArray }}
    </pre>
  </div>
</template>

<script>
export default {
  data() {
    return {
      localArray: this.parentArray
    };
  },
  props: {
    parentArray: {
      type: Array
    }
  }
};
</script>

<style scoped></style>
