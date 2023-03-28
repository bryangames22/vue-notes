<template>
  <div>
    <h3>Add a Note</h3>
    <form @submit.prevent="addNote">
      <div class="form-group">
        <label for="note">Note:</label>
        <textarea id="note" class="form-control" v-model="note"></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Add Note</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      note: ''
    }
  },
  methods: {
    addNote() {
      this.$emit('note-added', this.note);
      this.note = '';
    }
  }
}
</script>
