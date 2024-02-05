---
navigation:
  - vtiful-kernel-excel.getHandle.md: '« Vtiful\\Kernel\\Excel::getHandle'
  - vtiful-kernel-excel.insertFormula.md: 'Vtiful\\Kernel\\Excel::insertFormula »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::header'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::header

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::header — Записати заголовок

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::header(array $headerData)
```

Написати заголовок на аркуші.

### Список параметрів

`headerData`

Дані заголовка аркуша

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
    ->header(['name', 'age']);
?>
```
