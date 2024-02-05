---
navigation:
  - splfileobject.fputcsv.md: '« SplFileObject::fputcsv'
  - splfileobject.fscanf.md: 'SplFileObject::fscanf »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fread'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fread

(PHP 5 >= 5.5.11, PHP 7, PHP 8)

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

Повертає рядок, прочитаний із файлу або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример**SplFileObject::fread()\*\*\*\*

```php
<?php
// Чтение контента файла в строку
$filename = "/usr/local/something.txt";
$file = new SplFileObject($filename, "r");
$contents = $file->fread($file->getSize());
?>
```

### Примітки

> **Зауваження** :
> 
> Обратите внимание, что**SplFileObject::fread()** читає з поточної позиції покажчика файлу. Використовуйте [SplFileObject::ftell()](splfileobject.ftell.md) для пошуку поточної позиції покажчика та [SplFileObject::rewind()](splfileobject.rewind.md)(или[SplFileObject::fseek()](splfileobject.fseek.md)) зміни його позиції.

### Дивіться також

-   [fread()](function.fread.md) \- Бінарно-безпечне читання файлу
