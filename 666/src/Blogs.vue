<template>
  <div class="blogs">
    <h2>{{ blogTitle }}</h2>
    <button @click="changeTitle">Change Title</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Blogs",
  data() {
    return {
      blogTitle: "Blogs",
    };
  },
  methods: {},
  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts/")
      .then((response) => {
        console.log(response);
      });
  },
};
</script>