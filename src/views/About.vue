<template>
  <div class="about">
    <el-form>
      <el-form-item label="内容" label-width="50px">
        <quill-editor
          v-model="value"
          ref="myQuillEditor"
          :options="editorOption"
          @change="onEditorChange($event)"
        ></quill-editor>
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: "",
      editorOption: {
        placeholder: "请输入院校简介",
        theme: "snow",
        modules: {}
      }
    };
  },
  methods: {
    onEditorChange() {
      console.log(this.value);
    }
  }
};
</script>