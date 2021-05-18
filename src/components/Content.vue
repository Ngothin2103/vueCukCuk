<template>
  <div class="content">
    <div class="content__top">
      <div class="title"><h3>Danh sách nhân viên</h3></div>
      <div class="button__add">
        <button class="btn">Thêm nhân viên</button>
      </div>
    </div>
    <div class="content__bottom">
      <table class="tbl">
        <tbody>
          <th>
            <td>Mã nhân viên</td>
            <td>Họ và tên</td>
            <td>Giới tính</td>
            <td>Ngày sinh</td>
            <td>Điện thoại</td>
            <td>Email</td>
            <td>Chức vụ</td>
            <td>Phòng ban</td>
            <td>Mức lương cơ bản</td>
            <td>Tình trạng công việc</td>
          </th>
        </tbody>
      </table>
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
.content {
  position: absolute;
  top: 60px;
  left: 200px;
  width: calc(100% - 200px);
  height: calc(100vh - 60px);
}
.content__top {
  height: 60px;
  width: 100%;
  display: flex;
  align-items: center;
}
.title {
  width: 300px;
  height: 100%;
  line-height: 60px;
}
.title h3{
  margin-left: 10px;
}

.button__add {
  line-height: 60px;
}
.tbl td{
  width: 150px;
}
</style>>

