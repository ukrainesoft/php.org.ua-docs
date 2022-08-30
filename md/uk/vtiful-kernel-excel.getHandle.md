Отримати дескриптор

-   [« VtifulKernelExcel::fileName](vtiful-kernel-excel.filename.html)
    
-   [VtifulKernelExcel::header »](vtiful-kernel-excel.header.html)
    
-   [PHP Manual](index.html)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Отримати дескриптор
    

# VtifulKernelExcel::getHandle

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::getHandle — Отримати дескриптор

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::getHandle()
```

Отримати дескриптор текстового ресурсу xlsx.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ресурс

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

$handle = $file->getHandle();
?>
```