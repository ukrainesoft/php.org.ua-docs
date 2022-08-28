Кількість пам'яті

-   [« Vtiful\\Kernel\\Excel::autoFilter](vtiful-kernel-excel.autoFilter.html)
    
-   [Vtiful\\Kernel\\Excel::\_\_construct »](vtiful-kernel-excel.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)
    
-   Кількість пам'яті
    

# VtifulKernelExcel::constMemory

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::constMemory — Кількість пам'яті

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::constMemory(string $fileName, string $sheetName = ?)
```

Запис великого файлу з використанням пам'яті.

### Список параметрів

`fileName`

Ім'я файлу XLSX

`sheetName`

Назва листа

### Значення, що повертаються

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
  'path' => '/home/viest'
];

$fileObject = new \Vtiful\Kernel\Excel($config);

$file = $instance->constMemory('tutorial.xlsx', 'sheet');
?>
```