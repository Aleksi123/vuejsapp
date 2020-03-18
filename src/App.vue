<template>
  <div id="app">
    <TopBar />
    <NoteForm v-on:create-note="createNote" />
    <NoteList v-bind:notes="notes" v-on:del-note="deleteNote" />
  </div>
</template>

<script>
import TopBar from "./components/TopBar";
import NoteList from "./components/NoteList";
import NoteForm from "./components/NoteForm";

export default {
  name: "App",
  components: {
    TopBar,
    NoteList,
    NoteForm
  },
  data() {
    return {
      notes: [
        /* {
        id: 1,
        title: 'First Note Title',
        content: 'First Note Content'
      },
      {
        id: 2,
        title: 'Second Note Title',
        content: 'Second Note Content'
      } */
      ]
    };
  },
  methods: {
    deleteNote(i) {
      this.notes.splice(i, 1);
    },
    createNote(newNote) {
      this.notes = [...this.notes, newNote];
    }
  }
};
</script>

<style>
</style>
