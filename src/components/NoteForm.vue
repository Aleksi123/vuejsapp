<template>
  <div>
    <h3>Create Note:</h3>
    <form @submit="createNote">
      Note title:
      <b-form-input type="text" v-model="title" name="title" placeholder="Add note title"></b-form-input>Note content:
      <b-form-textarea
        type="text"
        rows="3"
        max-rows="6"
        v-model="content"
        name="content"
        placeholder="Add note content"
      ></b-form-textarea>
      <b-button type="submit" variant="primary" class="btn">Submit</b-button>
    </form>
  </div>
</template>

<script>
export default {
  name: "NoteForm",
  data() {
    return {
      title: "",
      content: ""
    };
  },
  methods: {
    createNote(e) {
      e.preventDefault();
      const newNote = {
        title: this.title,
        content: this.content
      };
      this.$emit("create-note", newNote);
      this.title = "";
      this.content = "";
    }
  }
};
</script>

<style>
</style>