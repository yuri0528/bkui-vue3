<template>
  <div class="style-demo">
    <!-- small -->
    <bk-select
      v-model="selectedValue"
      class="bk-select"
      size="small"
    >
      <bk-option
        v-for="(item, index) in datasource"
        :key="index"
        :value="item.value"
        :label="item.label"
      />
    </bk-select>
    <!-- default -->
    <bk-select
      v-model="selectedValue"
      class="bk-select"
    >
      <bk-option
        v-for="(item, index) in datasource"
        :key="index"
        :value="item.value"
        :label="item.label"
      />
    </bk-select>
    <!-- large -->
    <bk-select
      v-model="selectedValue"
      class="bk-select"
      size="large"
      multiple
      filterable
    >
      <bk-option
        v-for="(item, index) in datasource"
        :key="index"
        :value="item.value"
        :label="item.label"
      />
    </bk-select>
    <!-- simplicity small -->
    <bk-select
      v-model="selectedValue"
      class="bk-select"
      size="small"
      behavior="simplicity"
      multiple
      filterable
    >
      <bk-option
        v-for="(item, index) in datasource"
        :key="index"
        :value="item.value"
        :label="item.label"
      />
    </bk-select>
    <!-- simplicity large -->
    <bk-select
      v-model="selectedValue"
      class="bk-select"
      size="large"
      behavior="simplicity"
    >
      <bk-option
        v-for="(item, index) in datasource"
        :key="index"
        :value="item.value"
        :label="item.label"
      />
    </bk-select>
  </div>
</template>
<script setup>
  import { ref } from 'vue';
  const datasource = ref([
    {
      value: 'climbing',
      label: '爬山',
    },
    {
      value: 'running',
      label: '跑步',
    },
    {
      value: 'unknow',
      label: '未知',
    },
    {
      value: 'fitness',
      label: '健身',
    },
    {
      value: 'bike',
      label: '骑车',
    },
    {
      value: 'dancing',
      label: '跳舞',
    },
    {
      value: 'sleep',
      label: '睡觉',
      disabled: true,
    },
  ]);
  const selectedValue = ref('running');
</script>
<style scoped>
.style-demo {
  display: flex;
}

.bk-select {
  width: 200px;
  margin-right: 20px;
}
</style>

