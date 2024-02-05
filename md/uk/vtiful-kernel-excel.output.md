---
navigation:
  - vtiful-kernel-excel.mergeCells.md: '« Vtiful\\Kernel\\Excel::mergeCells'
  - vtiful-kernel-excel.setColumn.md: 'Vtiful\\Kernel\\Excel::setColumn »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::output'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::output

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::output - Висновок

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::output()
```

Виведення файлу xlsx на диск.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Шлях до файлу XLSX;

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

$path = $file->output();
?>
```
