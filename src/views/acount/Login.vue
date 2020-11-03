<template>
    <div class="acount">
        <div class="form-wrap">
            <a-form
              name="custom-validation"
              ref="ruleForm"
              v-bind="layout"
            >
              <a-form-item has-feedback label="账号" name="checkPass">
                  <a-input type="text" autocomplete="off" placeholder="请输出账号" />
              </a-form-item>
              <a-form-item has-feedback label="密码" name="pass">
                  <a-input type="password" autocomplete="off" placeholder="请输入密码" />
              </a-form-item>
              <a-form-item :wrapper-col="{ span: 16, offset: 4 }">
                <a-button type="primary" html-type="submit" block>
                    登录
                </a-button>
              </a-form-item>
              <a-anchor :affix="false">
                <a-anchor-link href="#components-anchor-demo-static" title="忘记密码" />
                <a-anchor-link
                  href="#components-anchor-demo-basic"
                  title="注册"
                  target="_blank"
                />
              </a-anchor>
            </a-form>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue';

export default defineComponent({
  name: 'Login',
  setup() {
    const formConfig = reactive({
      layout: {
        labelCol: { span: 24 },
        wrapperCol: { span: 24 },
      },
    });

    return {
      formConfig,
    };
  },
});
</script>

<style scoped lang="scss">
.acount {
    width: 100vw;
    height: 100vh;
    background: #282828;
    > .form-wrap {
        width: 60vw;
        margin: auto;
        padding-top: 300px;
        color: #fff;
    }
}
</style>
