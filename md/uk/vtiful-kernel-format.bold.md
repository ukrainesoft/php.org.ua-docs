---
navigation:
  - vtiful-kernel-format.align.md: '« Vtiful\\Kernel\\Format::align'
  - vtiful-kernel-format.italic.md: 'Vtiful\\Kernel\\Format::italic »'
  - index.md: PHP Manual
  - class.vtiful-kernel-format.md: Vtiful\\Kernel\\Format
title: 'Vtiful\\Kernel\\Format::bold'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Format::bold

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Format::bold — Напівжирний

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::bold(resource $handle)
```

Напівжирний формат [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.md)

### Список параметрів

`handle`

Дескриптор файлу xlsx

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

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
?>
```
