- [« zip_entry_compressionmethod](function.zip-entry-compressionmethod.md)
- [zip_entry_name »](function.zip-entry-name.md)

- [PHP Manual](index.md)
- [Функції Zip](ref.zip.md)
- Повертає реальний розмір файлу для дескриптора директорії

#zip_entry_filesize

(PHP 4 \>= 4.1.0, PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.0.0)

zip_entry_filesize — Повертає реальний розмір файлу для дескриптора
директорії

**Увага**

Ця функція була *Видалена* в PHP 8.0.0. Використання цієї функції не
рекомендується.

### Опис

**zip_entry_filesize**(resource `$zip_entry`): int\|false

Повертає реальний розмір заданого дескриптора директорії.

### Список параметрів

`zip_entry`
Дескриптор директорії, що повертається функцією
[zip_read()](function.zip-read.md).

### Значення, що повертаються

Реальний розмір дескриптора директорії або **`false`** у разі
виникнення помилки.

### Список змін

| Версія | Опис                                                                                                  |
|--------|-------------------------------------------------------------------------------------------------------|
| 8.0.0  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md). |

### Дивіться також

- [zip_open()](function.zip-open.md) - Відкриває ZIP-архів
- [zip_read()](function.zip-read.md) - Зчитує наступний запис у
ZIP-архіві
