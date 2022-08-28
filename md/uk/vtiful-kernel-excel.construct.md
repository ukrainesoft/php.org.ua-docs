Конструктор

-   [« Vtiful\\Kernel\\Excel::constMemory](vtiful-kernel-excel.constMemory.html)
    
-   [Vtiful\\Kernel\\Excel::data »](vtiful-kernel-excel.data.html)
    
-   [PHP Manual](index.html)
    
-   [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)
    
-   Конструктор
    

# VtifulKernelExcel::construct

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::construct — Конструктор

### Опис

public **VtifulKernelExcel::construct**(array `$config`

Конструктор [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)створити екземпляр.

### Список параметрів

`config`

Конфігурація експорту файлу XLSX

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$excelObject = new \Vtiful\Kernel\Excel($config);
?>
```