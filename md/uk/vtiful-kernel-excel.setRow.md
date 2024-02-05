---
navigation:
  - vtiful-kernel-excel.setColumn.md: '« Vtiful\\Kernel\\Excel::setColumn'
  - class.vtiful-kernel-format.md: Vtiful\\Kernel\\Format »
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::setRow'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::setRow

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::setRow — Встановити рядок

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::setRow(string $range, float $height, resource $format = ?)
```

Встановити формат рядка.

### Список параметрів

`range`

початкові та кінцеві рядки координат осередку

`height`

висота рядка

`format`

ресурс формату осередку

### Значення, що повертаються

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setRow('A1', 20, $boldStyle,)
    ->output();
```
