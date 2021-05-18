<template>
  <div class="header">
      <div class="header__left">
        <select name="" id="">
          <option value="">Nhà hàng biển đông</option>
          <option value="">Nhà hàng biển đông</option>
          <option value="">Nhà hàng biển đông</option>
        </select>
      </div>
      <div class="header__right">
        <div class="header__right__icon"></div>
        <div class="header__right__text">Ngô Canh Thìn</div>
        <div class="header__right__option"></div>
      </div>
  </div>
</template>
<script>
export default {
  data() {
    return {

    }
  }
}
</script>
<style scoped>
    .header{
        width: calc(100% - 200px);
        height: 60px;
        position: absolute;
        left: 200px;
        top: 0;
        display: flex;
        align-items: center;
        border-bottom: 1px solid gray;
    }
    .header__left{
      width: 200px;
      height: 60px;
      line-height: 60px;
      margin-left: 30px;
    }
    .header__left select{
      border-style: none;
    }
    .header__right{
      position: absolute;
      right: 0px;
      height: 100%;
      display: flex;    
      justify-content: right;
      align-items: center;
      margin-right: 30px;
    }
    .header__right__icon{
      width: 20px;
      height: 20px;
      background-image: url("../assets/icon/avatar-default.png");
      background-repeat: no-repeat;
      background-size: contain;
    }
    .header__right__text{
      margin-left: 5px;
      margin-right: 5px;
    }
    .header__right__option{
      width: 20px;
      height: 20px;
      background-image: url("../assets/icon/option.png");
      background-repeat: no-repeat;
      background-size: contain; 
    }
</style>

