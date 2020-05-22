<template>
    <div>
      这是商品列表
      <span>{{$route.params.goodsid}}</span><br/>
      <span>{{$route.params.name}}</span>
      <router-link to="/goods/title">显示商品标题</router-link>
      <router-link to="/goods/image">显示商品图片</router-link>
      <div>
        <router-view></router-view>
      </div>
      <button @click="jump">跳转到购物车</button>
      <router-link v-bind:to="{name:'cart',params:{cartId:123}}">跳转到购物车方式2</router-link>
    </div>
</template>

<script>
    export default {
        name: "GoodsList",
      methods:{
          jump(){
            //this.$router.push("/cart")
            this.$router.push({path:'/cart?goodsid=123'})
          }
      }
    }
</script>

<style scoped>

</style>
