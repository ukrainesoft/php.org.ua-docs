Курсив

-   [« Vtiful\\Kernel\\Format::bold](vtiful-kernel-format.bold.html)
    
-   [Vtiful\\Kernel\\Format::underline »](vtiful-kernel-format.underline.html)
    
-   [PHP Manual](index.html)
    
-   [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.html)
    
-   Курсив
    

# VtifulKernelFormat::italic

(PECL xlswriter >= 1.2.1)

VtifulKernelFormat::italic — Курсив

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::italic(resource $handle)
```

Формат курсиву [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.html)

### Список параметрів

`handle`

Дескриптор файлу xlsx

### Значення, що повертаються

Ресурс

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

$italicStyle = \Vtiful\Kernel\Format::italic($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $italicStyle)
    ->output();
?>
```