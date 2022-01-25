<template>
  <UploadButton style="margin: 0 10px" size="mini">mini</UploadButton>
  <UploadButton style="margin: 0 10px" size="small">small</UploadButton>
  <UploadButton style="margin: 0 10px" size="large" :success-duration="800"
    >这是一段较长的文字</UploadButton
  >
  <UploadButton style="margin: 0 10px">提交</UploadButton>
  <UploadButton style="margin: 0 10px" type="square">形状</UploadButton>
  <UploadButton style="margin: 0 10px" disabled>禁用</UploadButton>
</template>

<script lang="ts">
import UploadButton from 'arco-vue-uploadButton';

export default {
  name: 'BasicDemo',
  components: {
    UploadButton,
  },
};
</script>
