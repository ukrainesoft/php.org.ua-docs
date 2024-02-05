---
navigation:
  - class.curlsharehandle.md: « CurlShareHandle
  - curlfile.construct.md: 'CURLFile::\_\_construct »'
  - index.md: PHP Manual
  - book.curl.md: cURL
title: Клас CURLFile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас CURLFile

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Цей клас або [CURLStringFile](class.curlstringfile.md) можуть бути використані для завантаження файлу за допомогою опції **`CURLOPT_POSTFIELDS`**

Десеріалізація екземплярів **CURLFile**не допускается. Начиная с PHP 7.4.0, сериализация запрещена в первую очередь.

## Огляд класів

```classsynopsis

    
     class CURLFile
     {

    /* Свойства */
    
     public
     string
      $name = "";

    public
     string
      $mime = "";

    public
     string
      $postname = "";


    /* Методы */
    
   public __construct(string $filename, ?string $mime_type = null, ?string $posted_filename = null)

    public getFilename(): string
public getMimeType(): string
public getPostFilename(): string
public setMimeType(string $mime_type): void
public setPostFilename(string $posted_filename): void

   }
```

## Властивості

name

Шлях до файлу, який буде надіслано

mime

MIME-тип файла (по умолчанию`application/octet-stream`) .

postname

Ім'я файлу при надсиланні методом POST (за замовчуванням name)

## Дивіться також

-   [curl\_setopt()](function.curl-setopt.md)
-   [CURLStringFile](class.curlstringfile.md)

## Зміст

-   [CURLFile::\_\_construct](curlfile.construct.md)— Створює об'єкт CURLFile
-   [CURLFile::getFilename](curlfile.getfilename.md)— Повертає ім'я файлу на сервері
-   [CURLFile::getMimeType](curlfile.getmimetype.md) \- Повертає MIME-тип файлу
-   [CURLFile::getPostFilename](curlfile.getpostfilename.md)— Повертає ім'я файлу, що надсилається POST-запитом
-   [CURLFile::setMimeType](curlfile.setmimetype.md) \- Встановлює MIME-тип
-   [CURLFile::setPostFilename](curlfile.setpostfilename.md)— Встановлює ім'я файлу для надсилання методом POST
