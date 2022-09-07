---
navigation:
  - vtiful-kernel-excel.constMemory.md: '« VtifulKernelExcel::constMemory'
  - vtiful-kernel-excel.data.md: 'VtifulKernelExcel::data »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::construct'
---
# VtifulKernelExcel::construct

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::construct — Конструктор

### Опис

public **VtifulKernelExcel::construct**(array `$config`

Конструктор [VtifulKernelExcel](class.vtiful-kernel-excel.md)створити екземпляр.

### Список параметрів

`config`

Конфігурація експорту файлу XLSX

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$excelObject = new \Vtiful\Kernel\Excel($config);
?>
```
