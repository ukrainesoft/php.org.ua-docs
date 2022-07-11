- [« SplFileObject::fputcsv](splfileobject.fputcsv.md)
- [SplFileObject::fscanf »](splfileobject.fscanf.md)

- [PHP Manual](index.md)
- [SplFileObject](class.splfileobject.md)
- Читання з файлу

# SplFileObject::fread

(PHP 5 \>= 5.5.11, PHP 7, PHP 8)

SplFileObject::fread — Читання з файлу

### Опис

public **SplFileObject::fread**(int `$length`): string\|false

Зчитує задану кількість байт із файлу.

### Список параметрів

`length`
Кількість байт для читання.

### Значення, що повертаються

Повертає рядок, прочитаний з файлу або **`false`** у разі
виникнення помилки.

### Приклади

**Приклад #1 Приклад **SplFileObject::fread()****

` <?php// Читання контенту файла в рядок$filename = "/usr/local/something.txt";$file = new SplFileObject($filename, "r");$contents = $file->fread($ ->getSize());?> `

### Примітки

> **Примітка**:
>
> Зверніть увагу, що **SplFileObject::fread()** читає з поточної
> Позиції покажчика файлу. Використовуйте
> [SplFileObject::ftell()](splfileobject.ftell.md) для пошуку поточної
> позиції покажчика та
> [SplFileObject::rewind()](splfileobject.rewind.md) (або
> [SplFileObject::fseek()](splfileobject.fseek.md)) для зміни його
> Позиції.

### Дивіться також

- [fread()](function.fread.md) - Бінарно-безпечне читання файлу
