<template>
  <div id="app">
    <b-container class="container">
      <b-row>
        <b-col>
          <h1>Markdown</h1>
          <b-form-textarea
            class="info"
            id="textarea"
            v-model="text"
            placeholder="Write something..."
            rows="15"
          ></b-form-textarea>
        </b-col>
        <b-col>
          <h1>Preview</h1>
          <vue-markdown class="info" :source="text">{{ text }}</vue-markdown>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import VueMarkdown from "vue-markdown";
export default {
  name: "App",
  components: { VueMarkdown },
  data() {
    return {
      text: ""
    };
  }
};
</script>
<style scoped>
.container {
  margin-top: 40px;
}
.info {
  margin-top: 30px;
}
</style>
