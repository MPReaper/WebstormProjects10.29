<template>
  <div class="body-wrapper">
    <layout>
      <div class="container">
        <international-title></international-title>
        <european2017></european2017>
      </div>

    </layout>
  </div>

</template>

<script>
  import Layout from '../components/Layout/Layout.vue'
  import European2017 from '../components/International/European2017.vue'
  import InternationalTitle from '../components/International/InternationalTitle.vue'
  import Photo from '../components/Index/Photo.vue'

  export default {
    name: 'index-page',
    components: {
      Layout,
      InternationalTitle,
      European2017,
      Photo
    },
    data() {
      return {}
    },
    created() {
      this.menu();
    },
    methods: {
      menu() {
        window.scrollTo(0, 0);
      }
    }
  }
</script>
