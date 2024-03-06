<script setup>
import FileUpload from "primevue/fileupload";

import Card from "primevue/card";
</script>

<template>
  <Card class="custom-card">
    <template #title>
      <div>Upload the script you want to test</div>
    </template>
    <template #footer>
      <div>
        <FileUpload
          mode="basic"
          name="demo[]"
          url="/api/upload"
          accept="image/*"
          :maxFileSize="1000000"
          @upload="onUpload"
        />
      </div>
    </template>
  </Card>
</template>

<style scoped>
.custom-card {
  height: 150px;
  width: 400px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: center;
}
</style>
