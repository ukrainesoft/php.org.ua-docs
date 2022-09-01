---
navigation:
  - vtiful-kernel-excel.data.html: '« VtifulKernelExcel::data'
  - vtiful-kernel-excel.getHandle.html: 'VtifulKernelExcel::getHandle »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.html: VtifulKernelExcel
title: 'VtifulKernelExcel::fileName'
---
# VtifulKernelExcel::fileName

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::fileName — Створити назву файлу

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::fileName(string $fileName, string $sheetName = ?)
```

Створити новий файл XLSX та аркуш у ньому.

### Список параметрів

`fileName`

Ім'я файлу XLSX

`sheetName`

Назва листа

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.html)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->fileName('tutorial.xlsx', 'sheet');
?>
```
