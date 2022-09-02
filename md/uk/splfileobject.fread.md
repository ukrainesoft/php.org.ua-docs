---
navigation:
  - splfileobject.fputcsv.md: '« SplFileObject::fputcsv'
  - splfileobject.fscanf.md: 'SplFileObject::fscanf »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fread'
---
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
> Зверніть увагу, що **SplFileObject::fread()** читає з поточної позиції покажчика файлу. Використовуйте [SplFileObject::ftell()](splfileobject.ftell.md) для пошуку поточної позиції покажчика та [SplFileObject::rewind()](splfileobject.rewind.md) (або [SplFileObject::fseek()](splfileobject.fseek.md)) Зміни його позиції.

### Дивіться також

-   [fread()](function.fread.md) - Бінарно-безпечне читання файлу
