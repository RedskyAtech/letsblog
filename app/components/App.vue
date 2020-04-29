<template>
  <Page>
    <!-- <ActionBar title="Welcome to NativeScript-Vue!"/> -->
    <GridLayout columns="*" rows="*" class="main-container">
      <Button col="0" row="0" class="blog-button" :text="readBlog" @tap="onReadBlog()"></Button>
      <Button col="0" row="1" class="blog-button" :text="addBlog" @tap="onAddBlog()"></Button>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
export default {
  data() {
    return {
      readBlog: "Read blog",
      addBlog: "Add blog"
    };
  },
  methods: {
    onReadBlog() {
      // this.$navigateTo("ReadBlog");
    },
    onAddBlog() {
      // this.$navigateTo("AddBlog");
    }
  }
};
</script>

<style scoped>
/* ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    } */

.main-container {
  background: linear-gradient(#53ba82, #000000);
}

.blog-button {
  width: 55%;
  height: 35;
  margin: 20 0 0 5%;
  color: #ffffff;
  background-color: #f99620;
  font-size: 14%;
  font-weight: 500;
  padding: 0;
  border-radius: 5;
  border-width: 1;
  border-color: #f99620;
}

.blog-button:highlighted {
  background-color: #ffffff;
  border-color: #f99620;
  color: #f99620;
}
</style>
