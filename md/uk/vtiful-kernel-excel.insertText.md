---
navigation:
  - vtiful-kernel-excel.insertImage.md: '« Vtiful\\Kernel\\Excel::insertImage'
  - vtiful-kernel-excel.mergeCells.md: 'Vtiful\\Kernel\\Excel::mergeCells »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::insertText'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::insertText

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::insertText — Вставити текст

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::insertText(    int $row,    int $column,    int|float|string $data,    string $format = ?)
```

Вставити текст у комірку.

### Список параметрів

`row`

рядок осередку

`column`

стовпець осередку

`data`

дані для запису

`format`

формат рядка

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

$file = $excel->fileName("free.xlsx")
    ->header(['name', 'money']);

for ($index = 0; $index < 10; $index++) {
    $file->insertText($index+1, 0, 'viest');
    $file->insertText($index+1, 1, 10000, '#,##0');
}

$textFile->output();
```
