---
navigation:
  - curlfile.setpostfilename.md: '« CURLFile::setPostFilename'
  - curlstringfile.construct.md: 'CURLStringFile::construct »'
  - index.md: PHP Manual
  - book.curl.md: cURL
title: Клас CURLStringFile
---
# Клас CURLStringFile

(PHP 8> = 8.1.0)

## Вступ

Клас **CURLStringFile** дозволяє завантажувати файл прямо із змінної. Він схожий на [CURLFile](class.curlfile.md)але працює з вмістом файлу, а не з його ім'ям. Цей клас або [CURLFile](class.curlfile.md) слід використовувати для завантаження вмісту файлу за допомогою **`CURLOPT_POSTFIELDS`**

## Огляд класів

```synopsis

     
    

    
     
      class CURLStringFile
     
     {

    /* Свойства */
    
     public
     string
      $data;

    public
     string
      $postname;

    public
     string
      $mime;


    /* Методы */
    
   public __construct(string $data, string $postname, string $mime = "application/octet-stream")

   }
```

## Властивості

data

Вміст для завантаження.

postname

Ім'я файлу, який буде використовуватися в завантажених даних.

mime

MIME-тип файлу (за замовчуванням `application/octet-stream`

## Дивіться також

-   [curlsetopt()](function.curl-setopt.md)
-   [CURLFile](class.curlfile.md)

## Зміст

-   [CURLStringFile::construct](curlstringfile.construct.md) — Створює об'єкт CURLStringFile
