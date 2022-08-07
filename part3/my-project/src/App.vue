<template>
  <div id="app">
    <div class="container">
      <component-header
        v-bind:title="title"
        v-on:changeTitleEvent="handleChangeTitle"
      />
      <img src="./assets/logo.png" />
      <!-- // <HelloWorld/> -->
      <list-user
       v-bind:listUser="listUser"
       v-on:deleteUserEvent="handleDeleteUser" />
      <component-footer
        v-bind:title="title"
        v-on:changeTitleEvent="handleChangeTitle"
      />
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import ComponentHeader from "./components/ComponentHeader.vue";
import ComponentFooter from "./components/ComponentFooter.vue";
import ListUser from "./components/ListUser.vue";

export default {
  name: "App",

  data() {
    return {
      listUser: [
        { id: 10, email: "test1@gmail.com", active: true },
        { id: 11, email: "test2@gmail.com", active: true },
        { id: 12, email: "test3@gmail.com", active: false },
        { id: 13, email: "test4@gmail.com", active: false },
        { id: 14, email: "test5@gmail.com", active: false },
        { id: 15, email: "test6@gmail.com", active: false },
        { id: 16, email: "test7@gmail.com", active: false },
        { id: 17, email: "test8@gmail.com", active: false },
      ],
      title: "Hi bao lau chua gap",
    };
  },
  components: {
    HelloWorld,
    ComponentHeader,
    ComponentFooter,
    ListUser,
  },
  methods: {
    handleChangeTitle(data) {
      this.title = data.title;
    },
    handleDeleteUser(data) {
      let indexDelete = -1;
      this.listUser.forEach((u, idx) => {
        if (u.id === data.id) {
          indexDelete = idx;
        }
      });
      if (indexDelete != -1 ){
        this.listUser.splice(indexDelete, 1)
      }
    }
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container {
  max-width: 1170px;
  margin: 0 auto;
  padding: 0 15px;
  min-height: 3000px;
}
</style>
