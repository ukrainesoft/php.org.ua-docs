---
navigation:
  - vtiful-kernel-excel.constMemory.md: '« Vtiful\\Kernel\\Excel::constMemory'
  - vtiful-kernel-excel.data.md: 'Vtiful\\Kernel\\Excel::data »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::\_\_construct

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::\_\_construct — Конструктор

### Опис

public **Vtiful\\Kernel\\Excel::\_\_construct**(array`$config`) .

Конструктор[Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)створити екземпляр.

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
