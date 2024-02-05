---
navigation:
  - vtiful-kernel-excel.insertText.md: '« Vtiful\\Kernel\\Excel::insertText'
  - vtiful-kernel-excel.output.md: 'Vtiful\\Kernel\\Excel::output »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::mergeCells'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::mergeCells

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::mergeCells — Об'єднати осередки

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::mergeCells(string $scope, string $data)
```

Об'єднати комірки.

### Список параметрів

`scope`

початкові та кінцеві рядки координат осередку

`data`

дані рядки

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

$excel->fileName("test.xlsx")
        ->mergeCells('A1:C1', 'Merge cells')
        ->output();
```
