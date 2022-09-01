---
navigation:
  - vtiful-kernel-excel.construct.html: '« VtifulKernelExcel::construct'
  - vtiful-kernel-excel.filename.html: 'VtifulKernelExcel::fileName »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.html: VtifulKernelExcel
title: 'VtifulKernelExcel::data'
---
# VtifulKernelExcel::data

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::data — Записати дані

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::data(array $data)
```

Записати дані до таблиці.

### Список параметрів

`data`

Дані листа

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age'])
    ->data([
      ['viest', 23],
      ['wjx', 23],
    ]);
?>
```
