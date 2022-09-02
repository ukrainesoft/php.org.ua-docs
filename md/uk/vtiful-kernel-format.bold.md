---
navigation:
  - vtiful-kernel-format.align.md: '« VtifulKernelFormat::align'
  - vtiful-kernel-format.italic.md: 'VtifulKernelFormat::italic »'
  - index.md: PHP Manual
  - class.vtiful-kernel-format.md: VtifulKernelFormat
title: 'VtifulKernelFormat::bold'
---
# VtifulKernelFormat::bold

(PECL xlswriter >= 1.2.1)

VtifulKernelFormat::bold — Напівжирний

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::bold(resource $handle)
```

Напівжирний формат [VtifulKernelFormat](class.vtiful-kernel-format.md)

### Список параметрів

`handle`

Дескриптор файлу xlsx

### Значення, що повертаються

Ресурс

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$excel  = new \Vtiful\Kernel\Excel($config);

$fileObject = $excel->fileName('tutorial01.xlsx');
$fileHandle = $fileObject->getHandle();

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
?>
```
