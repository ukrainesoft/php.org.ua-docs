---
navigation:
  - vtiful-kernel-excel.data.md: '« Vtiful\\Kernel\\Excel::data'
  - vtiful-kernel-excel.getHandle.md: 'Vtiful\\Kernel\\Excel::getHandle »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::fileName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::fileName

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::fileName — Створити назву файлу

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

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->fileName('tutorial.xlsx', 'sheet');
?>
```
