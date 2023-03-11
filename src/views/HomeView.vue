<template>
  <div v-for="(item, index) in data" :key="index">
    <div>{{ item.title }}</div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
  data() {
    return {
      data: [],
    };
  },
  methods: {
    fetchData() {
      fetch("https://fakestoreapi.com/products")
        .then((res) => res.json())
        .then((data) => {
          console.log(data);
          this.data = data;
        });
    },
  },
  created() {
    this.fetchData();
  },
  mounted() {},
};
</script>
