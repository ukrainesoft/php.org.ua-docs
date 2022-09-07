---
navigation:
  - class.vtiful-kernel-excel.md: « VtifulKernelExcel
  - vtiful-kernel-excel.autoFilter.md: 'VtifulKernelExcel::autoFilter »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::addSheet'
---
# VtifulKernelExcel::addSheet

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::addSheet — Додати лист

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::addSheet(string $sheetName)
```

Створіть новий аркуш у файлі xlsx.

### Список параметрів

`sheetName`

Ім'я аркуша

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age'])
    ->data([
        ['viest', 23],
        ['wjx', 23]
    ]);

$file->addSheet('sheet_two')
    ->header(['name', 'age'])
    ->data([
        ['james', 33],
        ['king', 33]
    ]);

$file->output();
?>
```
