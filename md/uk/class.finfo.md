---
navigation:
  - function.mime-content-type.md: « mime\_content\_type
  - finfo.buffer.md: 'finfo::buffer »'
  - index.md: PHP Manual
  - book.fileinfo.md: FileInfo
title: Клас finfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас finfo

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

## Вступ

Цей клас надає об'єктно-орієнтований інтерфейс до функцій fileinfo.

## Огляд класів

```classsynopsis

    
     class finfo
     {

    /* Методы */
    
   public __construct(int $flags = FILEINFO_NONE, ?string $magic_database = null)

    public buffer(string $string, int $flags = FILEINFO_NONE, ?resource $context = null): string|false
public file(string $filename, int $flags = FILEINFO_NONE, ?resource $context = null): string|false
public set_flags(int $flags): bool

   }
```

## Зміст

-   [finfo::buffer](finfo.buffer.md) \- Псевдонім finfo\_buffer()
-   [finfo::\_\_construct](finfo.construct.md) \- Псевдонім finfo\_open
-   [finfo::file](finfo.file.md) \- Псевдонім finfo\_file()
-   [finfo::set\_flags](finfo.set-flags.md) \- Псевдонім finfo\_set\_flags()
