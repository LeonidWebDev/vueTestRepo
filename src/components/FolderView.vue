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
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.folder{
  line-height: 160%;
  font-size: 130%;
  color: #C70554;

  @media (min-width: 992px) {
    display: inline-block;
    width: 25%;
  }
  
  @media (max-width: 992px) {
    display: inline-block;
    width: 33%;
  }

  @media (max-width: 768px) {
    display: inline-block;
    width: 50%;
    
  }

  @media (max-width: 576px) {
    display: block;
    width: 100%;
  }
 
}
</style>
