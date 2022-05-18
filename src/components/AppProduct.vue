<template>
  <div class="product" :style="{ 'border-color': getColor() }">
    <img :src="productObj.src" alt="" />
    <h4>{{ productObj.titolo }}</h4>
    <small>Tempo di cottura {{ productObj.cottura }} min</small>
  </div>
</template>

<script>
export default {
  name: "AppProduct",
  // Passare i valori come un'oggetto unico in due modi: object notation oppure array di stringhe
  props: {
    productObj: Object,
  },
  //   props: ["productObj"]

  // Passare i valori separatamente in due modi: object notatiom o array di stringhe
  //   props: {
  //     img: String,
  //     title: String,
  //     cottura: Number
  //   },

  //   props: ["img", "title"],
  methods: {
    getColor: function () {
      let color;
      if (this.productObj.tipo === "lunga") {
        color = "blue";
      } else if (this.productObj.tipo === "corta") {
        color = "green";
      } else {
        color = "red";
      }
      return color;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.product {
  width: calc(100% / 4 - 4px);
  background-color: white;
  padding: 1rem 0.5rem;
  margin: 2px;
  border: 2px solid;
  //
  //   &.corta {
  //       border: 2px solid green;
  //   }
  //
  //   &.lunga {
  //       border: 2px solid blue;
  //   }
  //
  //   &.cortissima {
  //       border: 2px solid red;
  //   }

  h4 {
    font-size: 0.8rem;
    color: $brand-primary-color;
    text-align: center;
  }

  small {
    display: inline-block;
    text-align: center;
    font-size: 0.7rem;
    font-weight: 300;
    line-height: 0.8rem;
  }
}
</style>