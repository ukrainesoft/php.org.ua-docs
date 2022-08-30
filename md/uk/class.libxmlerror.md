Клас libXMLError

-   [« Предопределённые константы](libxml.constants.html)
    
-   [Функції libxml »](ref.libxml.html)
    
-   [PHP Manual](index.html)
    
-   [libxml](book.libxml.html)
    
-   Клас libXMLError
    

# Клас libXMLError

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Містить різну інформацію про помилки, що викидаються libxml. Коди помилок описані в офіційній [» xmlError API документации](http://www.xmlsoft.org/html/libxml-xmlerror.html)

## Огляд класів

```synopsis



    
     
      class libXMLError
     
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

Важливість помилки (одна з наступних констант: **`LIBXML_ERR_WARNING`** **`LIBXML_ERR_ERROR`** або **`LIBXML_ERR_FATAL`**

code

Код помилки

column

Стовпець, у якому сталася помилка.

> **Зауваження**
> 
> Ця властивість реалізована в libxml не до кінця, тому в більшості випадків повертатиметься `0`

message

Повідомлення про помилку, якщо є.

file

Ім'я файлу чи порожній рядок, якщо XML завантажувався з рядка.

line

Рядок, в якому сталася помилка.