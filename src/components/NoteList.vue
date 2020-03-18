<template>
  <div>
    <div v-for="note in notes" v-bind:key="note.id">
      <b-list-group>
        <Note v-bind:note="note" v-on:del-note="$emit('del-note', note.id)" />
      </b-list-group>
    </div>
  </div>
</template>

<script>
import Note from "./Note";

export default {
  name: "NoteList",
  components: {
    Note
  },
  props: ["notes"]
};
</script>

<style>
</style>