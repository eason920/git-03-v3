<template>
<div class="about">
  <h1>This is an about page</h1>
  <Card :title="envTitle"/>
  <Card title="Eason vue cli test"/>
</div>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
  components: {
    Card
  },
  created () {
    console.log('api is ', process.env.VUE_APP_API)
    console.log('path is ', process.env.VUE_APP_PATH)
  },
  data () {
    return {
      envTitle: process.env.VUE_APP_API
    }
  }
}
</script>
