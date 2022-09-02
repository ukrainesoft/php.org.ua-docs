---
navigation:
  - vtiful-kernel-format.italic.md: '« VtifulKernelFormat::italic'
  - refs.fileprocess.process.md: Модули для управления процессами программ »
  - index.md: PHP Manual
  - class.vtiful-kernel-format.md: VtifulKernelFormat
title: 'VtifulKernelFormat::underline'
---
# VtifulKernelFormat::underline

(PECL xlswriter >= 1.2.1)

VtifulKernelFormat::underline — Підкреслений

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::underline(resource $handle, int $style)
```

Підкреслений формат [VtifulKernelFormat](class.vtiful-kernel-format.md)

### Список параметрів

`handle`

Дескриптор файлу xlsx

`style`

Константа [VtifulKernelFormat](class.vtiful-kernel-format.md)

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

$underlineStyle = \Vtiful\Kernel\Format::underline($fileHandle, \Vtiful\Kernel\Format::UNDERLINE_SINGLE);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $underlineStyle)
    ->output();
?>
```
