<template>
  <div class="content">
    <div class="content__top">
      <div class="title"><h3>Danh sách nhân viên</h3></div>
      <div class="button__add">
        <button class="btn btn__themnv" @click="show_form">Thêm nhân viên</button>
      </div>
    </div>
    <div class="input__type">
        <div class="textbox">
          <input class="timkiem" type="text" placeholder="Tìm kiếm theo mã, tên hoặc số điện thoại">
        </div>
        <div class="textbox">
          <select class='phongban'>
            <option value="">Tất cả phòng ban</option>
          </select>
        </div>
        <div class="textbox">
          <select class="vitri">
            <option value="">Tất cả vị trí</option>
          </select>
        </div>
      </div>
      <br>
    <div class="content__bottom">
      <table class="tbl">
        <tbody>
          <th>
            <td width='100px'>Mã nhân viên</td>
            <td width='100px'>Họ và tên</td>
            <td width='100px'>Giới tính</td>
            <td width='100px'>Ngày sinh</td>
            <td width='100px'>Điện thoại</td>
            <td width='100px'>Email</td>
            <td width='100px'>Chức vụ</td>
            <td width='100px'>Phòng ban</td>
            <td width='100px'>Mức lương cơ bản</td>
            <td width='100px'>Tình trạng công việc</td>
          </th>
          <tr v-for="(items, index) in Employees" :key="index">
            <td class="EmployeeCode">{{items.EmployeeCode}}</td>
            <td class="EmployeeCode">{{items.FullName}}</td>
            <td class="EmployeeCode">{{items.Gender}}</td>
            <td class="EmployeeCode">{{items.DateOfBirth}}</td>
            <td class="EmployeeCode">{{items.PhoneNumber}}</td>
            <td class="EmployeeCode">{{items.Email}}</td>
            <td class="EmployeeCode">{{items.Address}}</td>
            <td class="EmployeeCode">null</td>
            <td class="EmployeeCode">null</td>
            <td class="EmployeeCode">null</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { bus } from '../main'
export default {
  name: "app",
  data() {
    return {
      Employees: [],
    };
  },
  created: async function() {
    await axios
      .get("http://cukcuk.manhnv.net/v1/Employees")
      .then((Response) => (this.Employees = Response.data));
  },
  methods:{
    show_form(){
      bus.$emit('show_form')

    }
  }
};
</script>
<style scoped>
.content {
  padding-left: 10px;
  padding-right: 10px;
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
.button__add {
  width: calc(100% - 300px);
  text-align: right;
}
.input__type {
  display: flex;
  width: 100%;
}
.timkiem{
  width: 300px;
}
td {
  border-bottom: darkgray solid 1px;
}

.btn__themnv{
  width: 120px;
}
</style>

