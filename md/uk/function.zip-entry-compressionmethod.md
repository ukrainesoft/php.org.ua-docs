- [«zip_entry_compressedsize](function.zip-entry-compressedsize.md)
- [zip_entry_filesize »](function.zip-entry-filesize.md)

- [PHP Manual](index.md)
- [Функції Zip](ref.zip.md)
- Повертає метод стиснення дескриптора директорії

#zip_entry_compressionmethod

(PHP 4 \>= 4.1.0, PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.0.0)

zip_entry_compressionmethod — Повертає метод стиснення дескриптора
директорії

**Увага**

Ця функція була *Видалена* в PHP 8.0.0. Використання цієї функції не
рекомендується.

### Опис

**zip_entry_compressionmethod**(resource `$zip_entry`): string\|false

Повертає метод стиснення дескриптора директорії, заданого в `zip_entry`.

### Список параметрів

`zip_entry`
Дескриптор директорії, що повертається функцією
[zip_read()](function.zip-read.md).

### Значення, що повертаються

Метод стиснення або **`false`** у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                  |
| ------ | ----------------------------------------------------------------------------------------------------- |
| 8.0.0  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md). |

### Дивіться також

- [zip_open()](function.zip-open.md) - Відкриває ZIP-архів
- [zip_read()](function.zip-read.md) - Зчитує наступний запис у
ZIP-архіві
