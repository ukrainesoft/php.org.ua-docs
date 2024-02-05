---
navigation:
  - vtiful-kernel-excel.filename.md: '« Vtiful\\Kernel\\Excel::fileName'
  - vtiful-kernel-excel.header.md: 'Vtiful\\Kernel\\Excel::header »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::getHandle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::getHandle

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::getHandle — Отримати дескриптор

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::getHandle()
```

Отримати дескриптор текстового ресурсу xlsx.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ресурс

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

$handle = $file->getHandle();
?>
```
