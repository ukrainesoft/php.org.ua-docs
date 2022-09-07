---
navigation:
  - vtiful-kernel-excel.output.md: '« VtifulKernelExcel::output'
  - vtiful-kernel-excel.setRow.md: 'VtifulKernelExcel::setRow »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::setColumn'
---
# VtifulKernelExcel::setColumn

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::setColumn — Встановити стовпець

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

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

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
