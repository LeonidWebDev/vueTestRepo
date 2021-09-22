<template>
  <p class="folder">{{name}}</p>
  <template v-for="folder in folders">
    <FolderView :name="folder.name" :folders="folder.folders" :files="folder.files"/>
  </template>
  <template v-for="file in files">
    <FileView :name="file.name"/>
  </template>
</template>

<script>
import FileView from "./FileView";
export default {
  name: 'FolderView',
  components: {FileView},
  props: {
    name: String,
    folders:Array,
    files:Array
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.folder{
  display: block;
  width: 100%;
  font-weight: bold;
  font-size: 150%;
  line-height: 200%;
  border-bottom: 2px solid black;
  color: #ffffff;
  background-color: #000000;
}

.folder:nth-child(2n) {
  background-color: #242424;
}

.folder:first-child {
  font-size: 200%;
  line-height: 250%;
  background-color: #000000;
  color: #fc8600;
}
</style>
