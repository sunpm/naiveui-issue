<template>
  <n-space vertical :size="12">
    <n-space>
      <n-button @click="downloadCsv">
        导出 CSV（原始数据）
      </n-button>
    </n-space>
    <n-data-table
      ref="tableRef"
      :columns="columns"
      :data="data"
      :pagination="pagination"
      :bordered="false"
    />
  </n-space>
</template>

<script setup lang="ts">
import type {
  DataTableColumns,
  DataTableInst,
  DataTableRowData
} from 'naive-ui'
import { ref } from 'vue'

interface Song {
  key: number
  name: string
  age: number
  address: string
}

const columns: DataTableColumns<DataTableRowData> = [
  {
    title: 'Name',
    key: 'name',
    sorter: 'default',
  },
  {
    title: 'Age',
    key: 'age',
  },
  {
    title: 'Address',
    key: 'address',
  }
]

const data: Song[] = [
  {
    key: 1,
    name: 'Jim Green',
    age: 28,
    address: '11111111111111111111 \r\n 222222222222222222222'
  },
]

const tableRef = ref<DataTableInst>()

function downloadCsv() {
  return tableRef.value?.downloadCsv({ fileName: 'data-table' })
}

const pagination = false as const
</script>
