<template>
  <div class="blogs">
    <h2>{{ blogTitle }}</h2>
    <button @click="changeTitle">Change Title</button>
  </div>
</template>

<script>
export default {
  name: "Blogs",
  data() {
    return {
      blogTitle: "Blogs",
    };
  },
  methods: {
    changeTitle() {
      this.blogTitle = "Bernie Would Have Won";
    },
  },
  beforeCreate() {
    alert("its the hook");
  },
  created() {
    alert(" things have been created");
  },
  beforeUpdate() {
    alert("things are about to happen");
  },
};
</script>