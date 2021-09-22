<template>
      <p class="file">{{name}}</p>
</template>

<script>
export default {
  name: 'FileView',
  props: {
    name: String
  }
}
</script>

<style scoped lang="scss">
  .file {
  flex: 1 0 25%;
  font-weight: 300;
  line-height: 200%;
  color: #7ee639;
  border-bottom: 1px solid black;
  background-color: #777777;

  } 

  @media (max-width: 992px) {
    .file {
      flex: 1 0 33%;
    }
  }

  @media (max-width: 768px) {
    .file {
      flex: 1 0 50%;
    }
  }

  @media (max-width: 576px) {
    .file {
      flex: 1 0 100%;
    }
  }

</style>
