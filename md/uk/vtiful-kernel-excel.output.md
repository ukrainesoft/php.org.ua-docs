Висновок

-   [« Vtiful\\Kernel\\Excel::mergeCells](vtiful-kernel-excel.mergeCells.html)
    
-   [Vtiful\\Kernel\\Excel::setColumn »](vtiful-kernel-excel.setColumn.html)
    
-   [PHP Manual](index.html)
    
-   [Vtiful\\Kernel\\Excel](class.vtiful-kernel-excel.html)
    
-   Висновок
    

# VtifulKernelExcel::output

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::output - Висновок

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::output()
```

Виведення файлу xlsx на диск.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Шлях до файлу XLSX;

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$fileObject  = new \Vtiful\Kernel\Excel($config);

$file = $fileObject->fileName('tutorial.xlsx', 'sheet_one')
    ->header(['name', 'age'])
    ->data([
      ['viest', 23],
      ['wjx', 23],
    ]);

$path = $file->output();
?>
```