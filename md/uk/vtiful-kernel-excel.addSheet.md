---
navigation:
  - class.vtiful-kernel-excel.md: « Vtiful\\Kernel\\Excel
  - vtiful-kernel-excel.autoFilter.md: 'Vtiful\\Kernel\\Excel::autoFilter »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::addSheet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::addSheet

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::addSheet — Додати лист

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::addSheet(string $sheetName)
```

Створіть новий аркуш у файлі xlsx.

### Список параметрів

`sheetName`

Ім'я аркуша

### Значення, що повертаються

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)

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
