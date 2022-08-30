Напівжирний

-   [« VtifulKernelFormat::align](vtiful-kernel-format.align.html)
    
-   [VtifulKernelFormat::italic »](vtiful-kernel-format.italic.html)
    
-   [PHP Manual](index.html)
    
-   [VtifulKernelFormat](class.vtiful-kernel-format.html)
    
-   Напівжирний
    

# VtifulKernelFormat::bold

(PECL xlswriter >= 1.2.1)

VtifulKernelFormat::bold — Напівжирний

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::bold(resource $handle)
```

Напівжирний формат [VtifulKernelFormat](class.vtiful-kernel-format.html)

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

$boldStyle = \Vtiful\Kernel\Format::bold($fileHandle);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $boldStyle)
    ->output();
?>
```