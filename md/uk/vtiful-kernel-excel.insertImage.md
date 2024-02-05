---
navigation:
  - vtiful-kernel-excel.insertFormula.md: '« Vtiful\\Kernel\\Excel::insertFormula'
  - vtiful-kernel-excel.insertText.md: 'Vtiful\\Kernel\\Excel::insertText »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::insertImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::insertImage

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::insertImage — Вставити зображення

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::insertImage(int $row, int $column, string $localImagePath)
```

Вставте локальне зображення у комірку.

### Список параметрів

`row`

рядок осередку

`column`

стовпець осередку

`localImagePath`

шлях до локального зображення

### Значення, що повертаються

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName("free.xlsx");

$file->insertImage(5, 0, '/vagrant/ASW-G-66.jpg');

$file->output();
```
