<template>
  <div>
    <div>
      <table>
        <thead>
        <tr>
          <th>产品名称</th>
          <th>单价</th>
          <th>数量</th>
          <th>操作</th>
        </tr>
        </thead>
        <tbody>
        <tr v-for='item in products'>
          <td>iPhone</td>
          <td>5188</td>
          <td>1</td>
          <td>添加</td>
        </tr>
        </tbody>
      </table>
    </div>
    <div @click="addToCart(p)">添加</div>
  </div>

</template>

<script type="text/ecmascript-6">
  import {mapGetters, mapActions} from 'vuex'
  export default {
    data(){
      return {}
    },
    created(){
      this.$store.dispatch('getAllProducts')
    },
    computed: mapGetters({
      products: 'allProducts'
    }),
    methods: mapActions(
      ['addToCart']
    )
  }


</script>
<style lang="scss">

</style>
