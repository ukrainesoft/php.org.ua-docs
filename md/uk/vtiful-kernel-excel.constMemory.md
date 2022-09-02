---
navigation:
  - vtiful-kernel-excel.autoFilter.md: '« VtifulKernelExcel::autoFilter'
  - vtiful-kernel-excel.construct.md: 'VtifulKernelExcel::construct »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::constMemory'
---
# VtifulKernelExcel::constMemory

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::constMemory — Кількість пам'яті

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::constMemory(string $fileName, string $sheetName = ?)
```

Запис великого файлу з використанням пам'яті.

### Список параметрів

`fileName`

Ім'я файлу XLSX

`sheetName`

Назва листа

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->constMemory('tutorial.xlsx', 'sheet');
?>
```
