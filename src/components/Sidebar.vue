<template>
  <div class="sidebar">
    <div class="sidebar__top">
      <div class="sidebar__top__toggle"></div>
      <div class="sidebar__top__logo"></div>
    </div>
    <div class="sidebar__bottom">
      <div class="sidebar__list">
        <div class="sidebar__item__icon dashboard"></div>
        <div class="sidebar__item__text">Tổng quan</div>
      </div>
      <div class="sidebar__list">
        <div class="sidebar__item__icon report"></div>
        <div class="sidebar__item__text">Báo cáo</div>
      </div>
      <div class="sidebar__list">
        <div class="sidebar__item__icon dashboard"></div>
        <div class="sidebar__item__text">Mua hàng</div>
      </div>
      <div class="sidebar__list">
        <div class="sidebar__item__icon dic-employee"></div>
        <div class="sidebar__item__text">Danh mục nhân viên</div>
      </div>
      <div class="sidebar__list">
        <div class="sidebar__item__icon dic-employee"></div>
        <div class="sidebar__item__text">Danh mục khách hàng</div>
      </div>
      <div class="sidebar__list">
        <div class="sidebar__item__icon setting"></div>
        <div class="sidebar__item__text">Thiết lập hệ thống</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.sidebar {
  width: 200px;
  height: 100vh;
  border-right: 1px solid gray;
}
.sidebar__top {
  height: 60px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.sidebar__top__toggle {
  width: 30px;
  height: 30px;
  background-image: url("../assets/img/toggle.png");
  background-repeat: no-repeat;
  background-size: contain;
  margin-right: 10px;
}
.sidebar__top__logo {
  width: 120px;
  height: 30px;
  background-image: url("../assets/img/cukcuk-logo.png");
  background-repeat: no-repeat;
  background-size: contain;
}
.sidebar__bottom {
  height: calc(100% - 60px);
  width: 100%;
  padding-top: 10px;
}
.sidebar__list {
  display: flex;
  width: 100%;
  height: 50px;
  cursor: pointer;
  align-items: center;
}
.sidebar__list:hover {
  background-color: cyan;
}
.sidebar__item__icon{
  margin-left: 10px;
}

.dashboard {
  background-image: url("../assets/icon/dashboard.png");
}
.setting {
  background-image: url("../assets/icon/setting.png");
}
.report {
  background-image: url("../assets/icon/report.png");
}
.dic-employee {
  background-image: url("../assets/icon/dic-employee.png");
}
</style>

