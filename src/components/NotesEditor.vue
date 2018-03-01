<template>
  <div id="node-editor">
    <textarea class="form-control" v-model="textVal" @change="editNote({text: textVal})"></textarea>
  </div>
</template>
<script>
import {mapState, mapActions} from 'vuex'
export default {
  data () {
    return {
      textVal: ''
    }
  },
  computed: {
    ...mapState({
      activeNote: state => state.activeNote
    })
  },
  methods: {
    ...mapActions({
      editNote: 'editNote'
    })
  },
  watch: {
    activeNotes: () => {
      this.$data.textVal = this.activeNote.text
    }
  }
}
</script>
<style>
  .form-control {
    width: 400px;
    height: 200px;
    margin-top: 20px;
  }
</style>
