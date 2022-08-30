Вставити формулу розрахунку

-   [« VtifulKernelExcel::header](vtiful-kernel-excel.header.html)
    
-   [VtifulKernelExcel::insertImage »](vtiful-kernel-excel.insertImage.html)
    
-   [PHP Manual](index.md)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Вставити формулу розрахунку
    

# VtifulKernelExcel::insertFormula

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::insertFormula — Вставити формулу розрахунку

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::insertFormula(int $row, int $column, string $formula)
```

Вставити формулу розрахунку.

### Список параметрів

`row`

рядок осередку

`column`

стовпець осередку

`formula`

рядок формули

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

$file = $excel->fileName("free.xlsx")
    ->header(['name', 'money']);

for($index = 1; $index < 10; $index++) {
    $file->insertText($index, 0, 'viest');
    $file->insertText($index, 1, 10);
}

$file->insertText(12, 0, "Total");
$file->insertFormula(12, 1, '=SUM(B2:B11)'); // вставить формулу

$file->output();
```