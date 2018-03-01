<template>
  <div id="toolbar">
    <button type="button" @click="addNote">增加</button>
    <button type="button" @click="toggleFavorite">收藏</button>
    <button type="button" @click="deleteNote">删除</button>
  </div>
</template>
<script>
import {mapState, mapActions} from 'vuex'
export default {
  computed: {
    ...mapState({
      activeNote: state => state.activeNote
    })
  },
  methods: {
    ...mapActions({
      addNote: 'addNote',
      toggleFavorite: 'toggleFavorite',
      deleteNote: 'deleteNote'
    })
  }
}
</script>
