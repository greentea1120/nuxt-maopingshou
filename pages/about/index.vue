<template>
  <div>
    <!--<pre>{{project}}</pre>-->
    <div class="hello">hello wolrd</div>
    <!--<nuxt-link to="/">回到首页</nuxt-link>-->
  </div>

</template>
<script>
  import axios from 'axios'

  export default {
    asyncData ({ params }) {
      console.log(params)
    },
    created () {
      axios.get(`http://data.maopingshou.com/api`)
        .then((res) => {
          console.log(res.data)
        })
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  .hello
    color: blue





  </style>

