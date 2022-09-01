---
navigation:
  - function.mime-content-type.html: « mimecontenttype
  - finfo.buffer.html: 'finfo::buffer »'
  - index.html: PHP Manual
  - book.fileinfo.html: FileInfo
title: Клас finfo
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

-   [finfo::buffer](finfo.buffer.html) - Псевдонім finfobuffer()
-   [finfo::construct](finfo.construct.html) - Псевдонім finfoopen
-   [finfo::file](finfo.file.html) - Псевдонім finfofile()
-   [finfo::setflags](finfo.set-flags.html) - Псевдонім finfosetflags()
