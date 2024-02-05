---
navigation:
  - vtiful-kernel-excel.construct.md: '« Vtiful\\Kernel\\Excel::\_\_construct'
  - vtiful-kernel-excel.filename.md: 'Vtiful\\Kernel\\Excel::fileName »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::data'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::data

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::data — Записати дані

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::data(array $data)
```

Записати дані до таблиці.

### Список параметрів

`data`

Дані листа

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
      ['wjx', 23],
    ]);
?>
```
