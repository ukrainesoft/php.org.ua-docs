---
navigation:
  - vtiful-kernel-format.bold.html: '« VtifulKernelFormat::bold'
  - vtiful-kernel-format.underline.html: 'VtifulKernelFormat::underline »'
  - index.html: PHP Manual
  - class.vtiful-kernel-format.html: VtifulKernelFormat
title: 'VtifulKernelFormat::italic'
---
# VtifulKernelFormat::italic

(PECL xlswriter >= 1.2.1)

VtifulKernelFormat::italic — Курсив

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::italic(resource $handle)
```

Формат курсиву [VtifulKernelFormat](class.vtiful-kernel-format.html)

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

$italicStyle = \Vtiful\Kernel\Format::italic($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $italicStyle)
    ->output();
?>
```
