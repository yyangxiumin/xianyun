<template>
  <div class="default">
    <!-- 头部组件 -->
    <Header />

    <nuxt />
    
    <!-- 页部组件 -->
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/header.vue'
import Footer from '@/components/footer.vue'
export default {
  components: {
    Header, Footer
  }
}
</script>

<style lang="less">
*{
  margin: 0;
  padding: 0;
}
a {
  text-decoration: none;
  color: inherit
}
ul,li,ol {
  list-style: none;
}
em, i{
  font-style: normal
}
a:hover{
  color: inherit
}
</style>