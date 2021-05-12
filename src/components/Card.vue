<template>
  <div>
    User: {{ name }}
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    name: {
      type: String,
      default: 'John Doe'
    }
  },
  data () {
    return {
    }
  },
  mounted () {
    console.log('component mounted')
  }
}

</script>
