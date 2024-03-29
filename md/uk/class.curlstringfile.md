---
navigation:
  - curlfile.setpostfilename.md: '« CURLFile::setPostFilename'
  - curlstringfile.construct.md: 'CURLStringFile::\_\_construct »'
  - index.md: PHP Manual
  - book.curl.md: cURL
title: Клас CURLStringFile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас CURLStringFile

(PHP 8 >= 8.1.0)

## Вступ

Класс**CURLStringFile** дозволяє завантажувати файл прямо із змінної. Він схожий на [CURLFile](class.curlfile.md)але працює з вмістом файлу, а не з його ім'ям. Цей клас або [CURLFile](class.curlfile.md) слід використовувати для завантаження вмісту файлу за допомогою **`CURLOPT_POSTFIELDS`**

## Огляд класів

```classsynopsis

    
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

MIME-тип файла (по умолчанию`application/octet-stream`

## Дивіться також

-   [curl\_setopt()](function.curl-setopt.md)
-   [CURLFile](class.curlfile.md)

## Зміст

-   [CURLStringFile::\_\_construct](curlstringfile.construct.md)— Створює об'єкт CURLStringFile
