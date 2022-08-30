Встановити стовпець

-   [« VtifulKernelExcel::output](vtiful-kernel-excel.output.html)
    
-   [VtifulKernelExcel::setRow »](vtiful-kernel-excel.setRow.html)
    
-   [PHP Manual](index.html)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Встановити стовпець
    

# VtifulKernelExcel::setColumn

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::setColumn — Встановити стовпець

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::setColumn(string $range, float $width, resource $format = ?)
```

Встановити формат шпальти.

### Список параметрів

`range`

початкові та кінцеві рядки координат осередку

`width`

ширина стовпця

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
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
```