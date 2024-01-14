# [ml-table-column](https://github.com/menglong-li/MlTableColumn)

### 简介
基于`vue3` `element plus` 组件库的 `el-table-column` 组件, 支持根据列内容自适应列宽。
省去人力计算宽度步骤。
![](https://github.com/menglong-li/MlTableColumn/blob/main/about.gif)
### 安装
```
npm install ml-table-column
```

### 使用
> 注意: 需要事先引入 `Vue` 和 `Element-UI` 依赖库, 并在 `<el-table></el-table>` 组件下使用该组件
- 全局注册 main.js
```
import Vue from 'vue'
import {MlTableColumn} from 'ml-table-column'
app.use(MlTableColumn)
```

- 默认用法, 全部自适应列宽
```
// list.vue
<template>
  <el-table :data="data">
    <el-table-column label="列头1" prop="field1"></el-table-column>
    <ml-table-column label="列头2" prop="keys" />
    <ml-table-column label="操作">
      <template #default="scope">
        <el-button type="primary" link>编辑</el-button>
        <el-button type="danger" link>删除</el-button>
      </template>
    </ml-table-column>
  </el-table>
</template>
```

```
//单独引用
import MlTableColumn from 'ml-table-column'
<ml-table-column prop="address" label="Address" />
```
