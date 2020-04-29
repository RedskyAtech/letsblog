<template>
  <Page actionBarHidden="true">
    <!-- <ActionBar title="Welcome to NativeScript-Vue!"/> -->
    <GridLayout class="main-container">
      <StackLayout class="content-container" rows="auto,auto,auto,auto">
        <Image row="0" :src="appLogo" class="app-logo"></Image>
        <Label row="1" :text="appName" class="app-name"></Label>
        <Button
          row="2"
          class="blog-button"
          androidElevation="5"
          :text="listBlog"
          @tap="onListBlog()"
        ></Button>
        <Button row="3" class="blog-button" androidElevation="5" :text="addBlog" @tap="onAddBlog()"></Button>
      </StackLayout>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import ListBlogs from "./ListBlogs.vue";
import AddBlogs from "./AddBlogs.vue";
export default {
  data() {
    return {
      listBlog: "List blog",
      addBlog: "Add blog",
      appLogo: "res://logo",
      appName: "Let's Blog"
    };
  },
  methods: {
    onListBlog() {
      this.$navigateTo(ListBlogs);
    },
    onAddBlog() {
      this.$navigateTo(AddBlogs);
    }
  }
};
</script>

<style scoped>
.main-container {
  height: 100%;
  background: linear-gradient(#53ba82, #000000);
}

.content-container {
  height: auto;
  width: auto;
  vertical-align: middle;
}

.app-logo {
  width: 25%;
}

.app-name {
  font-size: 18%;
  color: #f7f7f7;
  font-weight: 500;
  text-align: center;
  margin-bottom: 10%;
}

.blog-button {
  width: 55%;
  height: 35;
  margin: 10 0 10 0;
  background-color: #f7f7f7;
  font-size: 14%;
  font-weight: 500;
  padding: 0;
  border-radius: 5;
  color: #000000;
}

.blog-button:highlighted {
  background-color: #53ba82;
  color: #f7f7f7;
}
</style>
