---
navigation:
  - vtiful-kernel-excel.addSheet.md: '« Vtiful\\Kernel\\Excel::addSheet'
  - vtiful-kernel-excel.constMemory.md: 'Vtiful\\Kernel\\Excel::constMemory »'
  - index.md: PHP Manual
  - class.vtiful-kernel-excel.md: Vtiful\\Kernel\\Excel
title: 'Vtiful\\Kernel\\Excel::autoFilter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Vtiful\\Kernel\\Excel::autoFilter

(PECL xlswriter >= 1.2.1)

Vtiful\\Kernel\\Excel::autoFilter — Додати автофільтр

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::autoFilter(string $scope)
```

Додавання автофільтра до аркуша.

### Список параметрів

`scope`

Початковий та кінцевий рядок координат осередку.

### Значення, що повертаються

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.md)

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
