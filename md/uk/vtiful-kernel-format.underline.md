---
navigation:
  - vtiful-kernel-format.italic.md: '« Vtiful\\Kernel\\Format::italic'
  - refs.fileprocess.process.md: Модулі для керування процесами програм »
  - index.md: PHP Manual
  - class.vtiful-kernel-format.md: Vtiful\\Kernel\\Format
title: 'Vtiful\\Kernel\\Format::underline'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Format::underline

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Format::underline — Підкреслений

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::underline(resource $handle, int $style)
```

Підкреслений формат [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.md)

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

$underlineStyle = \Vtiful\Kernel\Format::underline($fileHandle, \Vtiful\Kernel\Format::UNDERLINE_SINGLE);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $underlineStyle)
    ->output();
?>
```
