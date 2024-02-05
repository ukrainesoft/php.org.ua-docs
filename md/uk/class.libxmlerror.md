---
navigation:
  - libxml.constants.md: « Зумовлені константи
  - ref.libxml.md: Функції libxml »
  - index.md: PHP Manual
  - book.libxml.md: libxml
title: Клас LibXMLError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас LibXMLError

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Містить інформацію про помилки, які видає модуль libxml. Коди помилок описані в офіційній [» документації xmlError API](http://www.xmlsoft.org/html/libxml-xmlerror.md)

## Огляд класів

```classsynopsis



    
     
      class LibXMLError
     
     {


    /* Свойства */
    
     public
     int
      $level;

    public
     int
      $code;

    public
     int
      $column;

    public
     string
      $message;

    public
     string
      $file;

    public
     int
      $line;

   }
```

## Властивості

level

Важливість помилки (одна з наступних констант: **`LIBXML_ERR_WARNING`** **`LIBXML_ERR_ERROR`** або **`LIBXML_ERR_FATAL`**) .

code

Код помилки

column

Стовпець, у якому сталася помилка.

> **Зауваження** :
> 
> Ця властивість реалізована в libxml не до кінця, тому в більшості випадків повертатиметься

message

Повідомлення про помилку, якщо є.

file

Ім'я файлу чи порожній рядок, якщо XML завантажувався з рядка.

line

Рядок, в якому сталася помилка.
