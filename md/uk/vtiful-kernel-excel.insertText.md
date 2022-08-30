Вставити текст

-   [« VtifulKernelExcel::insertImage](vtiful-kernel-excel.insertImage.html)
    
-   [VtifulKernelExcel::mergeCells »](vtiful-kernel-excel.mergeCells.html)
    
-   [PHP Manual](index.html)
    
-   [VtifulKernelExcel](class.vtiful-kernel-excel.html)
    
-   Вставити текст
    

# VtifulKernelExcel::insertText

(PECL xlswriter >= 1.2.1)

VtifulKernelExcel::insertText — Вставити текст

### Опис

```methodsynopsis
public Vtiful\Kernel\Excel::insertText(    int $row,    int $column,    stringintdouble $data,    string $format = ?)
```

Вставити текст у комірку.

### Список параметрів

`row`

рядок осередку

`column`

стовпець осередку

`data`

дані для запису

`format`

формат рядка

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

for ($index = 0; $index < 10; $index++) {
    $file->insertText($index+1, 0, 'viest');
    $file->insertText($index+1, 1, 10000, '#,##0');
}

$textFile->output();
```