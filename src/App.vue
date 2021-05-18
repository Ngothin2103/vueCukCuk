<template>
  <div id="app">
    <Sidebar></Sidebar>
    <Header></Header>
    <Content></Content>
  </div>
</template>
<script>
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import Content from './components/Content.vue'

export default {
  components: { 
      Header,
      Sidebar,
      Content
  },
  data() {
    return {
        
    }
  }
}
</script>
<style>
  *{
    margin: 0px;
  }
  #app{
    margin: 0px;
  }
  .sidebar__item__icon{
  width: 20px;
  height: 20px;
  background-repeat: no-repeat;
  background-size: contain;
  margin-right: 10px;
}
.btn{
      width: 120px;
      background-color: green;
      height: 30px;
      color: white;
      border-style: none;
    }
</style>
