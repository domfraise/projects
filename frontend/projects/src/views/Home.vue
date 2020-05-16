<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <ResourceView/>
  </div>
</template>

<script>
// @ is an alias to /src
import ResourceView from '@/components/ResourceView.vue'

export default {
  name: 'Home',
  components: {
    ResourceView
  }
}
</script>
