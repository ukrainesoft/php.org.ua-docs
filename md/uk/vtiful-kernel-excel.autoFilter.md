---
navigation:
  - vtiful-kernel-excel.addSheet.md: '« VtifulKernelExcel::addSheet'
  - vtiful-kernel-excel.constMemory.md: 'VtifulKernelExcel::constMemory »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: VtifulKernelExcel
title: 'VtifulKernelExcel::autoFilter'
---
# VtifulKernelExcel::autoFilter

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::autoFilter — Додати автофільтр

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::autoFilter(string $scope)
```

Додавання автофільтра до аркуша.

### Список параметрів

`scope`

Початковий та кінцевий рядок координат осередку.

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.md)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $excel->fileName('test.xlsx')
        ->header(['name', 'age'])
        ->data($data)
        ->autoFilter('A1:B11')  // автофильтр
        ->output();
?>
```
