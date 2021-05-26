<template>
  <div class="acount">
    <div class="form-warp">
      <a-form ref="ruleForm" v-bind="formConfig.layout">

        <a-form-item class="user">
          <label>用户名</label>
          <a-input type="username" autocomplete="off" />
        </a-form-item>

        <a-form-item>
          <label>密码</label>
          <a-input type="password" autocomplete="off" />
        </a-form-item>

        <a-form-item>
          <Captcha/>
        </a-form-item>

        <a-form-item>
          <a-button type="primary" html-tupe="submit" block> 登录 </a-button>
        </a-form-item>
      </a-form>
      <div class="ft-12 text-center">
        <a href="" class="color-white">忘记密码</a>丨
        <a href="" class="color-white">注册</a>
        </div>
    </div>
  </div>
</template>
<script>
import { onMounted, reactive, toRefs } from "vue";
//局部组件导入
import Captcha from "@/components/Captcha";
export default {
  name: "login",
  //组件注册
  components:{Captcha},
  setup(props) {
    const formConfig = reactive({
      layout: {
        labelCol: { span: 4 },
        wrapperCol: { span: 24 },
      },
    });

    
    onMounted(()=>{})
    return {
      formConfig,
    };
  },
};
</script>

<style lang="scss">
@import "./styles.scss";
</style>
