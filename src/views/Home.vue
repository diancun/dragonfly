<template>
  <div class="container">
    <main-header @changeSearch="changeSearch" />
    <main-content :searchTxt='searchTxt' />
  </div>
</template>

<script lang="ts">
import mainHeader from './components/main-header.vue'
import mainContent from './components/main-content.vue'
import { ref } from 'vue'
export default {
  components: {
    mainHeader,
    mainContent
  },
  setup () {
    const searchTxt = ref('')
    const changeSearch = (val: string) => {
      searchTxt.value = val
    }
    return {
      searchTxt,
      changeSearch
    }
  }
}
</script>

<style scoped lang="less">
  .container{
    width: 100%;
    min-height: 100vh;
    background-color: #F7F9FA;
  }
</style>
