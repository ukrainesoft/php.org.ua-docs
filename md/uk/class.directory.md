---
navigation:
  - dir.constants.md: « Зумовлені константи
  - directory.close.md: 'Directory::close »'
  - index.md: PHP Manual
  - book.dir.md: Каталоги
title: Клас Directory
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Directory

(PHP 4, PHP 5, PHP 7, PHP 8)

## Вступ

Примірники класу **Directory** створюються за допомогою виклику функції [dir()](function.dir.md), а не при помощи оператора[new](language.oop5.basic.md#language.oop5.basic.new)

## Огляд класів

```classsynopsis

    
     class Directory
     {

    /* Свойства */
    
     public
     readonly
     string
      $path;

    public
     readonly
     resource
      $handle;


    /* Методы */
    
   public close(): void
public read(): string|false
public rewind(): void

   }
```

## Властивості

path

Каталог, який було відкрито.

handle

Може використовуватися з іншими функціями каталогів, такими як [readdir()](function.readdir.md) [rewinddir()](function.rewinddir.md) і [closedir()](function.closedir.md)

## список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Властивості path та handle тепер доступні лише для читання. |

## Зміст

-   [Directory::close](directory.close.md)— Закриває дескриптор каталогу
-   [Directory::read](directory.read.md)— Отримує елемент із дескриптора каталогу
-   [Directory::rewind](directory.rewind.md)— Переміщує дескриптор каталогу на початок каталогу
