---
navigation:
  - class.vtiful-kernel-format.md: « Vtiful\\Kernel\\Format
  - vtiful-kernel-format.bold.md: 'Vtiful\\Kernel\\Format::bold »'
  - index.md: PHP Manual
  - class.vtiful-kernel-format.md: Vtiful\\Kernel\\Format
title: 'Vtiful\\Kernel\\Format::align'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Format::align

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Format::align — Вирівнювання

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::align(resource $handle, int $style)
```

Встановити вирівнювання осередку

### Список параметрів

`handle`

Дескриптор файлу xlsx

`style`

Константа[Vtiful\\Kernel\\Format](class.vtiful-kernel-format.md)

### Значення, що повертаються

Ресурс

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

$alignStyle = \Vtiful\Kernel\Format::align($fileHandle, \Vtiful\Kernel\Format::FORMAT_ALIGN_LEFT);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $align)
    ->output();
?>
```
