- [«mime_content_type](function.mime-content-type.md)
- [finfo::buffer »](finfo.buffer.md)

- [PHP Manual](index.md)
- [FileInfo](book.fileinfo.md)
- Клас finfo

# Клас finfo

(PHP 5 \>= 5.3.0, PHP 7, PHP 8, PECL fileinfo \>= 0.1.0)

## Вступ

Цей клас надає об'єктно-орієнтований інтерфейс до функцій
fileinfo.

## Огляд класів

class **finfo** {

/\* Методи \*/

public [\_\_construct](finfo.construct.md)(int `$flags` =
**`FILEINFO_NONE`**, ?string `$magic_database` = **`null`**)

public [buffer](finfo.buffer.md)(string `$string`, int `$flags` =
**`FILEINFO_NONE`**, ?resource `$context` = **`null`**): string\|false

public [file](finfo.file.md)(string `$filename`, int `$flags` =
**`FILEINFO_NONE`**, ?resource `$context` = **`null`**): string\|false

public [set_flags](finfo.set-flags.md)(int `$flags`): bool

}

## Зміст

- [finfo::buffer](finfo.buffer.md) - Псевдонім finfo_buffer()
- [finfo::\_\_construct](finfo.construct.md) - Псевдонім finfo_open
- [finfo::file](finfo.file.md) - Псевдонім finfo_file()
- [finfo::set_flags](finfo.set-flags.md) - Псевдонім
finfo_set_flags()
