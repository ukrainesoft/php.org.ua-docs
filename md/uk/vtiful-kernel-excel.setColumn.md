---
navigation:
  - vtiful-kernel-excel.output.md: '« Vtiful\\Kernel\\Excel::output'
  - vtiful-kernel-excel.setRow.md: 'Vtiful\\Kernel\\Excel::setRow »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::setColumn'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::setColumn

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::setColumn — Встановити стовпець

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::setColumn(string $range, float $width, resource $format = ?)
```

Встановити формат шпальти.

### Список параметрів

`range`

початкові та кінцеві рядки координат осередку

`width`

ширина стовпця

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
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
```
