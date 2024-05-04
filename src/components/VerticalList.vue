<template>
  <div class="vertical-list">
    <HorizontalList
      v-for="item in items"
      :key="item.id"
      :count="getRandomInt(10, 20)"
    />
  </div>
</template>

<script>
import HorizontalList from "./HorizontalList.vue";

export default {
  name: "VerticalList",
  components: {
    HorizontalList,
  },
  data() {
    return {
      items: Array.from(
        { length: this.getRandomInt(100, 150) },
        (_, index) => ({ id: index })
      ),
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
.vertical-list {
  display: flex;
  flex-direction: column;
}
</style>
