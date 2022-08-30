Встановити рядок

-   [« VtifulKernelExcel::setColumn](vtiful-kernel-excel.setColumn.html)
    
-   [VtifulKernelFormat »](class.vtiful-kernel-format.html)
    
-   [PHP Manual](index.md)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Встановити рядок
    

# VtifulKernelExcel::setRow

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::setRow — Встановити рядок

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::setRow(string $range, float $height, resource $format = ?)
```

Встановити формат рядка.

### Список параметрів

`range`

початкові та кінцеві рядки координат осередку

`height`

висота рядка

`format`

ресурс формату осередку

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.html)

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
    ->setRow('A1', 20, $boldStyle,)
    ->output();
```