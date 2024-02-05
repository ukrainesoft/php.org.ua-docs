---
navigation:
  - vtiful-kernel-format.bold.md: '« Vtiful\\Kernel\\Format::bold'
  - vtiful-kernel-format.underline.md: 'Vtiful\\Kernel\\Format::underline »'
  - index.md: PHP Manual
  - class.vtiful-kernel-format.md: Vtiful\\Kernel\\Format
title: 'Vtiful\\Kernel\\Format::italic'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Format::italic

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Format::italic — Курсив

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::italic(resource $handle)
```

Формат курсива[Vtiful\\Kernel\\Format](class.vtiful-kernel-format.md)

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

$italicStyle = \Vtiful\Kernel\Format::italic($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $italicStyle)
    ->output();
?>
```
