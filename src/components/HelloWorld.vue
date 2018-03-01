<template>
  <div class="hello">
    <toolbar></toolbar>
    <notes-list></notes-list>
    <notes-editor></notes-editor>
  </div>
</template>

<script>
import Toolbar from './Toolbar.vue'
import NotesList from './NotesList.vue'
import NotesEditor from './NotesEditor.vue'
export default {
  name: 'HelloWorld',
  components: {
    Toolbar,
    NotesList,
    NotesEditor
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  float: left;
}
a {
  color: #42b983;
}
</style>
