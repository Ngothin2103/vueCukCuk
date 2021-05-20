<template>
  <div class="form" v-if="isShow">
    <form action="">
      <div class="form__header">
        <h3>Thông tin khách hàng</h3>
      </div>
      <div class="form__content">
        <div class="form__content__left">
          <div class="img__person"></div>
        </div>
      </div>
      <div class="form__footer"></div>
    </form>
    <button @click="showTest">Tesst</button>
  </div>
</template>

<script>
import {bus} from '../main'
export default {
  name: "Form",
  data() {
    return {
        isShow : false
    };
  },
  methods:{
     moform(){
          this.isShow = !this.isShow
     },
  },
  created(){
      bus.$on('show_form',this.moform)
  }
};

</script>

<style scoped>
.form {
  padding: 15px;
  width: 500px;
  position: absolute;
  top: 50%;
  left: 50%;
}
</style>
