<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-4 sidebar">
          <Sidebar />
        </div>

        <div class="col-me-8 content">
          <Messages />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
import Sidebar from "../sidebar/Sidebar";
import Messages from "../messages/Messages";

export default {
  name: "Chat",
  components: {
    Sidebar,
    Messages
  },
  computed: {
    // ...mapState(["messagesScrollHeight"])
  },
  methods: {
    // scrollCallback() {
    // console.log("Chat: ", this.messagesScrollHeight);
    // window.scrollTo({
    //   top: this.messagesScrollHeight
    //   // behavior: "smooth"
    // });
    // }
  }
};
</script>

<style scoped>
.sidebar {
  padding-top: 2em;
  display: block;
  float: left;
  position: fixed;
  width: 33.5%;
  height: 100%;
  background: #000;
  overflow-x: hidden;
}

.content {
  margin-left: 34%;
  display: block;
  float: left;
  width: 66%;
}
</style>
