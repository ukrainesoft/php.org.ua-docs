Підкреслений

-   [« Vtiful\\Kernel\\Format::italic](vtiful-kernel-format.italic.html)
    
-   [Модули для управления процессами программ »](refs.fileprocess.process.html)
    
-   [PHP Manual](index.html)
    
-   [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.html)
    
-   Підкреслений
    

# VtifulKernelFormat::underline

(PECL xlswriter >= 1.2.1)

VtifulKernelFormat::underline — Підкреслений

### Опис

```methodsynopsis
public Vtiful\Kernel\Format::underline(resource $handle, int $style)
```

Підкреслений формат [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.html)

### Список параметрів

`handle`

Дескриптор файлу xlsx

`style`

Константа [Vtiful\\Kernel\\Format](class.vtiful-kernel-format.html)

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

$underlineStyle = \Vtiful\Kernel\Format::underline($fileHandle, \Vtiful\Kernel\Format::UNDERLINE_SINGLE);

$fileObject->header(['name', 'age'])
    ->data([['viest', 21]])
    ->setColumn('A:A', 200, $underlineStyle)
    ->output();
?>
```