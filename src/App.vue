<template>
  <div id="app">
    <div
      v-for="item in list"
      :key="item.id"
      >
      <Card :name="item.name" />
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Card from '@/components/Card'
export default {
  name: 'App',
  components: {
    Card
  },
  data () {
    return {
      list: []
    }
  },
  mounted () {
    axios.get('https://jsonplaceholder.typicode.com/users')
      .then((res) => {
        this.list = res.data
      })
    console.log('fetch finished')
    this.$nextTick(() => {
      console.log('next tick')
    })
  }

}
</script>
