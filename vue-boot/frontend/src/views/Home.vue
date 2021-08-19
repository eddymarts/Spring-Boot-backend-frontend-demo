<template>
  <div class="home">
    <hi> {{ title }} </hi>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data () {
    return {
      title: ''
    }
  },
  mounted () {
    fetch('http:localhost:8085')
      .then(response => {
        return response.text()
      })
      .then(data => {
        this.title = data
      })
  }
}
</script>
