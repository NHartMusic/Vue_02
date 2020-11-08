<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
    <AllFriends :friends="friends" @delete="deleteFriend" />
    <OnlineFriends :friends="friends" />
  </div>
</template>

<script>
import Navbar from "./Navbar";
import AllFriends from "./AllFriends";
import OnlineFriends from "./OnlineFriends";
export default {
  name: "app",
  components: {
    Navbar,
    OnlineFriends,
    AllFriends,
  },
  data() {
    return {
      title: "Smell My Hair Daddy Joe ;)",
      friends: [
        { name: "Hunter", online: true },
        { name: "Elizabeth", online: false },
        { name: "Kamala", online: true },
        { name: "Donald", online: false },
      ],
    };
  },
  methods: {
    deleteFriend(payload) {
      console.log(payload);
      this.friends = this.friends.filter((friend) => {
        return friend.name !== payload.name;
      });
    },
  },
};
</script>

<style>
h1 {
  color: red;
  font-weight: normal;
  text-align: center;
}
</style>
