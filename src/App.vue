<template>
  <FolderView name="$" :folders="folders" :files="files" />
</template>

<script>
import FolderView from './components/FolderView.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    FolderView
  },
  data: () => data
}
</script>

<style lang="scss">
body, p {
  margin: 0px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  text-align: center;
  font-size: 16px;
  min-width: 320px;
  min-height: 100vh;
  background-color: #140420;

  @media (min-width: 992px) {
    font-size: 32px;;
  }
  @media (max-width: 992px) {
    font-size: 28px;
  }

  @media (max-width: 768px) {
      font-size: 24px;
      
      
  }

  @media (max-width: 576px) {
      font-size: 16px;
  }
}
</style>
