---
navigation:
  - vtiful-kernel-excel.autoFilter.md: '« Vtiful\\Kernel\\Excel::autoFilter'
  - vtiful-kernel-excel.construct.md: 'Vtiful\\Kernel\\Excel::\_\_construct »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::constMemory'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::constMemory

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::constMemory — Кількість пам'яті

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

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->constMemory('tutorial.xlsx', 'sheet');
?>
```
