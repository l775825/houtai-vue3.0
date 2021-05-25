<template>
  <div class="acount">
    <div class="form-warp">
      <a-form-model
        ref="ruleForm"
        v-bind="layout"
      >
        <a-form-model-item>
          <a-input type="password" autocomplete="off" />
        </a-form-model-item>

        <a-form-model-item :wrapper-col="{ span: 14, offset: 4 }">
          <a-button type="primary">
            Submit
          </a-button>
        </a-form-model-item>
      </a-form-model>
    </div>
  </div>
</template>
<script>
export default {
  name: "login",
};
</script>

<style lang="scss">
@import "./styles.scss";
</style>
