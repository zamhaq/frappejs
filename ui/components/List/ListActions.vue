<template>
  <div class="frappe-list-actions d-flex justify-content-between align-items-center p-3 border-bottom">
    <h5 class="m-0">{{ doctype }} List</h5>
    <button v-if="showDelete" class="btn btn-danger btn-sm" @click="$emit('delete')">Delete</button>
    <button v-if="showNew" class="btn btn-primary btn-sm" @click="$emit('new')">New</button>
    <button v-if="showArchive" class="btn btn-primary btn-sm" @click="$emit('archiveList')">Archive</button>
    <button v-if="showCreateKanban" class="btn btn-primary btn-sm" @click="$emit('createKanban')">Create Kanban</button>
  </div>
</template>
<script>
export default {
  props: {
    doctype: String,
    showDelete: Number,
    showCreateKanban: Boolean,
    showNew: {
      type: Boolean,
      default: true
    },
    showArchive: {
      type: Boolean,
      default: false
    }
  }
};
</script>
