<template>
  <div>
    <b-list-group-item>
        Title: {{note.title}}<br>
        Content: {{note.content}}<br>
        <b-button @click="$emit('del-note', note.id)" variant="danger">Delete</b-button>
    </b-list-group-item>
  </div>
</template>

<script>
export default {
  name: "Note",
  props: ["note"]
};
</script>

<style>
</style>