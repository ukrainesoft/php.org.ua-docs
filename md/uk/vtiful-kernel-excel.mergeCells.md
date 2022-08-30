Об'єднати комірки

-   [« VtifulKernelExcel::insertText](vtiful-kernel-excel.insertText.html)
    
-   [VtifulKernelExcel::output »](vtiful-kernel-excel.output.html)
    
-   [PHP Manual](index.html)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Об'єднати комірки
    

# VtifulKernelExcel::mergeCells

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::mergeCells — Об'єднати осередки

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::mergeCells(string $scope, string $data)
```

Об'єднати комірки.

### Список параметрів

`scope`

початкові та кінцеві рядки координат осередку

`data`

дані рядки

### Значення, що повертаються

Екземпляр [VtifulKernelExcel](class.vtiful-kernel-excel.html)

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$config = [
    'path' => './tests'
];

$excel = new \Vtiful\Kernel\Excel($config);

$excel->fileName("test.xlsx")
        ->mergeCells('A1:C1', 'Merge cells')
        ->output();
```