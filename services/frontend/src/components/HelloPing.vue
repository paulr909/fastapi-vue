<template>
  <div>
    <h1>{{ msg }}</h1>
    <p>Yep that Vue route works.</p>
  </div>
</template>

<script>
import axios from "axios";
import { defineComponent } from "vue";

export default defineComponent({
  name: "HelloPing",
  data() {
    return {
      msg: "",
    };
  },
  methods: {
    getMessage() {
      axios
        .get("/ping")
        .then((res) => {
          this.msg = res.data;
        })
        .catch((error) => {
          console.error(error);
        });
    },
  },
  created() {
    this.getMessage();
  },
});
</script>
