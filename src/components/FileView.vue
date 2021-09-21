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
.file{
  line-height: 150%;
  color: #FF7486;

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
