<template>
  <div>
    <button @focus="boo = true" @blur="boo = false">{{ mark }}</button>

    <div>{{ boo }}</div>
  </div>
</template>

<script>
export default {
  props: {
    mark: {
      type: String,
      default: "marker",
    },
    // boo: {
    //   type: Boolean,
    //   default: false,
    // },
  },
  methods: {
    testFun() {
      console.log(this.boo);
    },
  },
  data() {
    return {
      boo: false,
    };
  },
};
</script>

<style scoped>
/* button {
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 3px;
  color: #000;
  cursor: pointer;
  font-size: 14px;
  font-weight: bold;
  margin: 0;
  padding: 5px 10px;
  text-align: center;
  text-decoration: none;
  transition: all 0.2s ease-in-out;
}
button:active {
  background-color: red;
} */
</style>
