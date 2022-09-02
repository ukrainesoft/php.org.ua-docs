---
navigation:
  - vtiful-kernel-excel.insertText.md: '« VtifulKernelExcel::insertText'
  - vtiful-kernel-excel.output.md: 'VtifulKernelExcel::output »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::mergeCells'
---
# VtifulKernelExcel::mergeCells

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::mergeCells — Об'єднати осередки

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::mergeCells(string $scope, string $data)
```

Об'єднати комірки.

### Список параметрів

`scope`

початкові та кінцеві рядки координат осередку

`data`

дані рядки

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$excel->fileName("test.xlsx")
        ->mergeCells('A1:C1', 'Merge cells')
        ->output();
```
