---
navigation:
  - class.curlsharehandle.html: « CurlShareHandle
  - curlfile.construct.html: 'CURLFile::construct »'
  - index.html: PHP Manual
  - book.curl.html: cURL
title: Клас CURLFile
---
# Клас CURLFile

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Цей клас або [CURLStringFile](class.curlstringfile.html) можуть бути використані для завантаження файлу за допомогою опції **`CURLOPT_POSTFIELDS`**

Десеріалізація екземплярів **CURLFile** не допускається. Починаючи з PHP 7.4.0, серіалізація заборонена насамперед.

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

MIME-тип файлу (за замовчуванням `application/octet-stream`

postname

Ім'я файлу при надсиланні методом POST (за замовчуванням name)

## Дивіться також

-   [curlsetopt()](function.curl-setopt.html)
-   [CURLStringFile](class.curlstringfile.html)

## Зміст

-   [CURLFile::construct](curlfile.construct.html) — Створює об'єкт CURLFile
-   [CURLFile::getFilename](curlfile.getfilename.html) — Повертає ім'я файлу на сервер
-   [CURLFile::getMimeType](curlfile.getmimetype.html) - Повертає MIME-тип файлу
-   [CURLFile::getPostFilename](curlfile.getpostfilename.html) — Повертає ім'я файлу, що надсилається POST-запитом
-   [CURLFile::setMimeType](curlfile.setmimetype.html) - Встановлює MIME-тип
-   [CURLFile::setPostFilename](curlfile.setpostfilename.html) — Встановлює ім'я файлу для надсилання методом POST
