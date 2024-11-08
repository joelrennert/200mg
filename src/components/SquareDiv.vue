<template>
  <div
    class="square"
    :class="{ 'is-hovered': isHovered, clicked: isClicked }"
    @mouseover="onHover"
    @mouseleave="onLeave"
    @click="onClick"
  >
    200
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHovered: false,
      isClicked: false
    }
  },
  methods: {
    onHover() {
      this.isHovered = true
    },
    onLeave() {
      setTimeout(() => {
        this.isHovered = false
      }, 4000)
    },
    onClick() {
      this.isClicked = true
      setTimeout(() => {
        this.isClicked = false
      }, 1000) // Hide after 1 second
    }
  }
}
</script>

<style scoped>
.square {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.5rem;
  font-weight: 500;
  font-style: bold;
  padding: 30px;
  border-radius: 50%;
  background-color: #fffffe52;
  box-shadow:
    8px 8px 15px rgba(64, 67, 60, 0.2),
    -8px -8px 15px rgba(218, 215, 191, 0.3),
    8px 8px 15px rgba(64, 67, 60, 0.2),
    inset 5px 5px 15px rgba(255, 255, 255, 0.5),
    inset -5px -5px 15px rgba(0, 0, 0, 0.2);
  opacity: 0;
  transition: opacity 1s ease;
  background-color: #a0522d;
  color: #28364d86;
}

.square.is-hovered {
  opacity: 1;
  transition: opacity 0.1s ease-in-out;
  cursor: pointer;
}

.square.clicked {
  opacity: 0;
  transition: opacity 1s ease-out;
}
</style>
