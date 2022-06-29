<template>
  <div class="our-project">
    <h2>Our Project</h2>
    <div class="grid-container">
      <div
        v-for="(item, index) in listBox"
        :key="index"
        class="grid-item"
        :style="`background-color:${random_rgba()}`"
      ></div>
    </div>
    <button class="button-css" @click="addItem" type="button">See all</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      listBox: [1, 2, 3, 4, 5, 6],
    };
  },
  mounted() {},
  methods: {
    random_rgba() {
      var o = Math.round,
        r = Math.random,
        s = 255;
      return (
        "rgba(" +
        o(r() * s) +
        "," +
        o(r() * s) +
        "," +
        o(r() * s) +
        "," +
        r().toFixed(1) +
        ")"
      );
    },
    addItem(){
        this.listBox.push(7,8,9)
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.our-project {
  text-align: center;
  padding: 0 200px;
  .grid-container {
    display: grid;
    column-gap: 10px;
    row-gap: 10px;
    grid-template-columns: auto auto auto;
    padding: 10px;
    .grid-item {
      padding: 20px;
      font-size: 30px;
      height: 200px;
      text-align: center;
      transition: 0.3s;
      opacity: 0.5;
      &:hover{
        opacity: 1;
        cursor: pointer;
      }
    }
  }
  .button-css{
      background-color: white;
      border : 1px solid rgb(72, 209, 97);
      border-radius: 50px;
      padding: 10px 20px;
      &:hover{
          background-color: rgb(72, 209, 97);
          color: white;
      }
  }

}
</style>
