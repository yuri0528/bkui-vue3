<template>
  <div>
    <bk-input
      v-model="val"
      class="mb10"
      type="number"
      size="small"
      :min="1"
      :max="100"
      clearable
    />
    <bk-input
      v-model="val"
      class="mb10"
      type="number"
      :min="1"
      :max="100"
      clearable
    />
    <bk-input
      v-model="val"
      class="mb10"
      disabled
      type="number"
      size="large"
      :min="1"
      :max="100"
      clearable
    />
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  const val = ref(100);
</script>

<style lang="less">
  .mb10 {
    margin-bottom: 10px;
  }
</style>
