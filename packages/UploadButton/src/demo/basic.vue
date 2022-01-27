<template>
  <div class="wrap">
    <UploadButton style="margin: 0 10px" size="mini">mini</UploadButton>
    <UploadButton style="margin: 0 10px" size="small">small</UploadButton>
    <UploadButton style="margin: 0 10px">提交</UploadButton>
    <UploadButton style="margin: 0 10px" type="square">形状</UploadButton>
    <UploadButton style="margin: 0 10px" size="large" :success-duration="800"
      >这是一段较长的文字</UploadButton
    >
    <UploadButton style="margin: 0 10px" disabled>禁用</UploadButton>
  </div>
</template>

<script lang="ts">
// eslint-disable-next-line import/no-unresolved
import UploadButton from 'arco-vue-upload-button';

export default {
  name: 'BasicDemo',
  components: {
    UploadButton,
  },
};
</script>
<style>
.wrap {
  width: 100%;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
