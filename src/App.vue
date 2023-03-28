<template>
  <div class="container">
    <note-form @note-added="addNote"></note-form>
    <note-list :notes="notes"></note-list>
  </div>
</template>

<script>
import NoteForm from './components/NoteForm.vue';
import NoteList from './components/NoteList.vue';

export default {
  components: {
    NoteForm,
    NoteList
  },
  data() {
    return {
      notes: []
    }
  },
  methods: {
    addNote(note) {
      this.notes.push(note);
    }
  }
}
</script>

