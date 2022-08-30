Конструктор

-   [« VtifulKernelExcel::constMemory](vtiful-kernel-excel.constMemory.html)
    
-   [VtifulKernelExcel::data »](vtiful-kernel-excel.data.html)
    
-   [PHP Manual](index.md)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Конструктор
    

# VtifulKernelExcel::construct

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::construct — Конструктор

### Опис

public **VtifulKernelExcel::construct**(array `$config`

Конструктор [VtifulKernelExcel](class.vtiful-kernel-excel.html)створити екземпляр.

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