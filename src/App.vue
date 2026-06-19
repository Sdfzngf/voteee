<template>
  <Form :modelValue="items"></Form>
  <hr />
  <Result :modelValue="items"></Result>
</template>

<script setup lang="ts">
import Form from '@/components/form/Form.vue';
import Result from '@/components/result/Result.vue';
import { ref } from 'vue';
import { IItem } from '@/models/item';

const templateItems: IItem[] = [
  {
    id: '你对瑞神的评价?',
    type: 'selection',
    title: '你对瑞神的评价?',
    options: ['精彩极了', '还行', '糟糕透了'],
    result: {
      type: 'chart',
      chartType: 'doughnut'
    }
  },
  {
    id: '你对祥神的评价?',
    type: 'selection',
    title: '你对祥神的评价?',
    options: ['夯爆了', '一般', '拉完了'],
    result: {
      type: 'chart',
      chartType: 'doughnut'
    }
  },
  {
    id: '您今天吃了吗?',
    type: 'selection',
    title: '您今天吃了吗?',
    options: ['吃了', '没有', '不知道'],
    result: {
      type: 'chart',
      chartType: 'doughnut'
    }
  }
];
const items = ref(templateItems);
</script>

<style scoped></style>
