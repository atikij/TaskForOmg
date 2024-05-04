<template>
  <div
    class="square"
    @mouseover="isHover = true"
    @mouseleave="isHover = false"
    :style="{ transform: isHover ? 'scale(0.8)' : 'scale(1)' }"
  >
    {{ number }}
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Square",
  props: {
    number: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      isHover: false,
    };
  },
};
</script>

<style scoped>
.square {
  width: 100px;
  height: 100px;
  border: 2px solid black;
  border-radius: 10px;
  margin: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: transform 0.3s ease;
}
</style>
