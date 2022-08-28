Записати заголовок

-   [« Vtiful\\Kernel\\Excel::getHandle](vtiful-kernel-excel.getHandle.html)
    
-   [Vtiful\\Kernel\\Excel::insertFormula »](vtiful-kernel-excel.insertFormula.html)
    
-   [PHP Manual](index.html)
    
-   [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)
    
-   Записати заголовок
    

# VtifulKernelExcel::header

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::header — Записати заголовок

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::header(array $headerData)
```

Написати заголовок на аркуші.

### Список параметрів

`headerData`

Дані заголовка листа

### Значення, що повертаються

Екземпляр [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age']);
?>
```