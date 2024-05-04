<template>
  <div class="horizontal-list">
    <Square v-for="item in items" :key="item.id" :number="item.number" />
  </div>
</template>

<script>
import Square from "./Square.vue";

export default {
  name: "HorizontalList",
  components: {
    Square,
  },
  props: {
    count: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      items: Array.from({ length: this.count }, (_, index) => ({
        id: index,
        number: this.getRandomInt(1, 100),
      })),
    };
  },
  methods: {
    getRandomInt(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    },
  },
};
</script>

<style scoped>
.horizontal-list {
  display: flex;
  flex-wrap: nowrap;
  overflow-x: scroll;
  scrollbar-width: none;
  .square {
    flex: 0 0 auto;
  }
}
</style>
