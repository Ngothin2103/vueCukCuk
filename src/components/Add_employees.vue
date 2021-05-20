<template>
  <div class="form" v-if="isShow">
    <form action="">
      <div class="form__header">
        <h3>THÔNG TIN KHÁCH HÀNG</h3>
        <br />
        <br />
      </div>
      <div class="form__content">
        <div class="form__content__top">
          <div class="form__content__top__left"></div>
          <div class="form__content__top__right">
            <div class="infor">
              <div class="item">
                <div class="text">
                  Mã khách hàng<span class="note">(*)</span>
                </div>
                <input type="text" />
              </div>
              <div class="item">
                <div class="text">Họ và tên<span class="note">(*)</span></div>
                <input type="text" />
              </div>
            </div>
            <br />
            <div class="infor">
              <div class="item">
                <div class="text">Mã thẻ thành viên</div>
                <input type="text" />
              </div>
              <div class="item">
                <div class="text">Nhóm khách hàng</div>
                <select name="" id="">
                  <option value="">Nhóm khách hàng Misa</option>
                </select>
              </div>
            </div>
            <br />
            <div class="infor">
              <div class="item">
                <div class="text">Ngày sinh</div>
                <input type="date" />
              </div>
              <div class="item gioitinh">
                <div class="text">Giới tính</div>
                <div class="value__gender">
                  <input type="radio" id="male" name="gender" value="male" />
                  <label for="male">Nam</label><br />
                  <input
                    type="radio"
                    id="female"
                    name="gender"
                    value="female"
                  />
                  <label for="female">Nữ</label><br />
                  <input type="radio" id="other" name="gender" value="other" />
                  <label for="other">Khác</label>
                </div>
              </div>
            </div>
          </div>
        </div>
        <br />
        <div class="form__content__bottom">
          <div class="form__content__bottom__line">
            <div class="item item__left">
              <div class="text">Email</div>
              <input type="email" />
            </div>
            <div class="item">
              <div class="text">Số điện thoại<span class="note">(*)</span></div>
              <input type="text" />
            </div>
          </div>
          <br />
          <div class="form__content__bottom__line">
            <div class="item item__left">
              <div class="text">Tên công ty</div>
              <input type="text" />
            </div>
            <div class="item">
              <div class="text">Mã số thuế</div>
              <input type="text" placeholder="Mã số thuế của công ty" />
            </div>
          </div>
          <br />
          <div class="form__content__bottom__line">
            <div class="diachi">
              <div class="text">Địa chỉ</div>
              <input type="text" />
            </div>
          </div>
          <div class="form__content__bottom__down"></div>
        </div>
      </div>
      <div class="form__footer">
        <button @click="close_form" value="cancel" class="btn btn__huy">HỦY</button>
        <button class="btn btn__luu" type="submit">LƯU</button>
      </div>
    </form>
    <button @click="close_form" class="btn closeForm">X</button>
  </div>
</template>

<script>
import { bus } from "../main";
export default {
  name: "Form",
  data() {
    return {
      isShow: false,
    };
  },
  methods: {
    moform() {
      this.isShow = !this.isShow;
    },
    close_form(){
      this.isShow = !this.isShow;
    }
  },
  created() {
    bus.$on("show_form", this.moform);
  },
};
</script>

<style scoped>
.form {
  background-color: white;
  border: 1px solid black;
  width: 700px;
  height: 500px;
  position: absolute;
  top: 30%;
  left: 30%;
}
.closeForm {
  position: absolute;
  top: 0px;
  right: 0px;
  width: 25px;
  height: 25px;
  background-color: red;
}
.form__header{padding: 15px;}
.form__content{padding-left: 15px;}
.form__content__top {
  display: flex;
}
.form__content__top__left {
  background-image: url("../assets/img/default-avatar.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  width: 130px;
  height: 130px;
  border-radius: 50%;
  border: 1px solid gray;
}
.form__content__top__right {
  width: calc(100% - 130px);
}
.infor {
  margin-left: 15px;
  display: flex;
}
.item {
  margin-right: 15px;
}
.note {
  color: red;
}
.gioitinh {
  margin-left: 30px;
}
.value__gender {
  display: flex;
  margin-top: 5px;
}
.value__gender label {
  margin-right: 15px;
  line-height: 15px;
}
.form__content__bottom__line {
  display: flex;
}
.item__left {
  width: 70%;
}
.item__left input {
  width: 100%;
}
.diachi {
  width: calc(100% - 15px);
}
.diachi input {
  width: 100%;
}
.form__footer {
  margin:0px;
  bottom: 0px;
  width: 100%;
  position: absolute;
  background-color: #cccccc;
  text-align: right;
}
.form__footer button {
  width: 50px;
  height: 30px;
  margin: 10px;
}
.btn__huy {
  background-color: #cccccc;
  color: black;
  padding: 5px;
}
.btn__huy:hover{
  background-color: red;
}
</style>
