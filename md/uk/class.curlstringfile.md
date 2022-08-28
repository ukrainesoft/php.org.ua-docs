Клас CURLStringFile

-   [« CURLFile::setPostFilename](curlfile.setpostfilename.html)
    
-   [CURLStringFile::\_\_construct »](curlstringfile.construct.html)
    
-   [PHP Manual](index.html)
    
-   [cURL](book.curl.html)
    
-   Клас CURLStringFile
    

# Клас CURLStringFile

(PHP 8> = 8.1.0)

## Вступ

Клас **CURLStringFile** дозволяє завантажувати файл прямо із змінної. Він схожий на [CURLFile](class.curlfile.html)але працює з вмістом файлу, а не з його ім'ям. Цей клас або [CURLFile](class.curlfile.html) слід використовувати для завантаження вмісту файлу за допомогою **`CURLOPT_POSTFIELDS`**

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

-   [curl\_setopt()](function.curl-setopt.html)
-   [CURLFile](class.curlfile.html)

## Зміст

-   [CURLStringFile::\_\_construct](curlstringfile.construct.html) — Створює об'єкт CURLStringFile