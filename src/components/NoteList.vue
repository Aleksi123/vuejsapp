<template>
  <div>
    <div v-for="note in notes" v-bind:key="notes.indexOf(note)">
      <b-list-group>
        <b-list-group-item>
          Title: {{note.title}}
          <br />
          Content: {{note.content}}
          <br />
          <b-button v-on:click="$emit('del-note',notes.indexOf(note))" variant="danger">Delete</b-button>
        </b-list-group-item>
      </b-list-group>
    </div>
  </div>
</template>

<script>
export default {
  name: "NoteList",
  props: ["notes"]
};
</script>

<style>
</style>