<template>
  <div>
    <h3>Notes</h3>
    <ul>
      <li v-for="(note, index) in notes" :key="index">{{ note }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    notes: Array
  }
}
</script>
