---
navigation:
  - vtiful-kernel-excel.insertFormula.md: '« VtifulKernelExcel::insertFormula'
  - vtiful-kernel-excel.insertText.md: 'VtifulKernelExcel::insertText »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::insertImage'
---
# VtifulKernelExcel::insertImage

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::insertImage — Вставити зображення

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::insertImage(int $row, int $column, string $localImagePath)
```

Вставте локальне зображення у комірку.

### Список параметрів

`row`

рядок осередку

`column`

стовпець осередку

`localImagePath`

шлях до локального зображення

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName("free.xlsx");

$file->insertImage(5, 0, '/vagrant/ASW-G-66.jpg');

$file->output();
```
