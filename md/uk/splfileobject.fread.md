Читання з файлу

-   [« SplFileObject::fputcsv](splfileobject.fputcsv.html)
    
-   [SplFileObject::fscanf »](splfileobject.fscanf.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Читання з файлу
    

# SplFileObject::fread

(PHP 5> = 5.5.11, PHP 7, PHP 8)

SplFileObject::fread — Читання з файлу

### Опис

```methodsynopsis
public SplFileObject::fread(int $length): string|false
```

Зчитує задану кількість байт із файлу.

### Список параметрів

`length`

Кількість байт для читання.

### Значення, що повертаються

Повертає рядок, прочитаний із файлу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад **SplFileObject::fread()****

```php
<?php
// Чтение контента файла в строку
$filename = "/usr/local/something.txt";
$file = new SplFileObject($filename, "r");
$contents = $file->fread($file->getSize());
?>
```

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що **SplFileObject::fread()** читає з поточної позиції покажчика файлу. Використовуйте [SplFileObject::ftell()](splfileobject.ftell.html) для пошуку поточної позиції покажчика та [SplFileObject::rewind()](splfileobject.rewind.html) (або [SplFileObject::fseek()](splfileobject.fseek.html)) Зміни його позиції.

### Дивіться також

-   [fread()](function.fread.html) - Бінарно-безпечне читання файлу