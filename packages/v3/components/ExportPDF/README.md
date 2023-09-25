## ExportPDF

Export content as a PDF file.

## Usage

```vue
<template>
  <MdEditor v-model="text" :toolbars="toolbars">
    <template #defToolbars>
      <ExportPDF :modelValue="text">
        <template #trigger> pdf </template>
      </ExportPDF>
    </template>
  </MdEditor>
</template>

<script setup>
import { ref } from 'vue';
import { MdEditor } from 'md-editor-v3';
import 'md-editor-v3/lib/style.css';

import { ExportPDF } from '@vavt/v3-extension';

const text = ref('# PDF');
const toolbars = ['bold', 0, 'underline'];
</script>
```

## Props

| name | type | default | description |
| --- | --- | --- | --- |
| title | `string` | 'Export as PDF' or '导出为 PDF' | Shown as a tooltip text when the mouse moves over |
| width | `string` | '870px' | Width of component `Modal` |
| height | `string` | '600px' | Height of component `Modal` |
| modalTitle | `string` | 'Export as PDF' or '导出为 PDF' | Title of component `Modal` |
| modelValue | `string` | '' | Conten need to be exported |
| fileName | `string` | 'md' | Exported file name |
| exportBtnText | `string` | 'Export' or '导出' |  |

## Slots

| name | type | default | description |
| --- | --- | --- | --- |
| trigger | `string \| VNode \| JSX.Element` | '' | Content displayed in the toolbar |