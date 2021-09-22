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

  body {
    min-width: 320px;
    min-height: 100vh;
    background-color: #000000;
    margin: 0;
  }

  p {
    margin: 0px;
  }

  #app {
    
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;

    text-align: center;
    font-size: 33px;
    min-width: 320px;
    min-height: 100vh;
    max-width: 1200px;
    border-left: 3px solid white;
    border-right: 3px solid white;
    box-shadow: 0 0 40px rgb(102, 255, 0);
    margin: 0px auto;
    
    display: flex;
    flex-wrap: wrap;
    
    @media (max-width: 992px) {
      font-size: 33px;
    }

    @media (max-width: 768px) {
        font-size: 33px;
    }

    @media (max-width: 576px) {
        font-size: 22px;
    }
  }

</style>
