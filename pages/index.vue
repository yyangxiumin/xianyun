<template>
  <div>
    <div class="block">
      <el-carousel height="700px">
        <el-carousel-item v-for="(item, index) in banners" :key="index">
          <div class="banner" 
          :style="`background:url(${$axios.defaults.baseURL + item.url}) center center no-repeat`">
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      // 轮播图数据
      banners: [
        // "http://157.122.54.189:9095/assets/images/th01.jfif",
        // "http://157.122.54.189:9095/assets/images/th02.jfif"
      ],
      // 搜索框tab栏选项
      // options: [
      //   {

      //   }
      // ]
    }
  },
  mounted () {
    this.$axios({
      url: "/scenics/banners"
    }).then(res=>{
      const {data} = res.data
      this.banners = data
    })
  }
}
</script>

<style lang="less" scoped>
.banner {
   height: 700px;
}
</style>