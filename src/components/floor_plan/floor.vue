<template>
  <div class="data">
    <p>Click in the div element below to get the x (horizontal) and y (vertical) coordinates of the mouse pointer, when it is clicked.</p>

    <div class="data-content" @click="showCoords(event)">
      <p id="demo"></p>
    </div>

    <p>
      <strong>Tip:</strong> Try to click different places in the div.
    </p>
  </div>
</template>

<script>
export default {
  methods: {
    showCoords: function(event) {
      var cX = event.clientX;
      var sX = event.screenX;
      var cY = event.clientY;
      var sY = event.screenY;
      var coords1 = "client - X: " + cX + ", Y coords: " + cY;
      var coords2 = "screen - X: " + sX + ", Y coords: " + sY;
      document.getElementById("demo").innerHTML = coords1 + "<br>" + coords2;
    }
  }
};
</script>

<style lang="scss" scoped>
.data {
  background-color: white;
  &-content {
    width: 500px;
    height: 300px;
    border: 1px solid black;
    text-align: center;
  }
}
</style>