Перевіряє, чи підтримується метод стиснення libzip

-   [« ZipArchive::getStreamName](ziparchive.getstreamname.html)
    
-   [ZipArchive::isEncryptionMethodSupported »](ziparchive.isencryptionmethoddupported.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Перевіряє, чи підтримується метод стиснення libzip
    

# ZipArchive::isCompressionMethodSupported

(PHP >= 8.0.0, PECL zip >= 1.19.0)

ZipArchive::isCompressionMethodSupported — Перевіряє, чи підтримується метод стиснення libzip

### Опис

```methodsynopsis
public static ZipArchive::isCompressionMethodSupported(int $method, bool $enc = true): bool
```

Перевіряє, чи підтримується метод стиснення libzip.

### Список параметрів

`method`

Метод стиснення, одна з констант **`ZipArchive::CM_*`**

`enc`

Якщо **`true`** перевірка на стиск, інакше перевірка на декомпресію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише в тому випадку, якщо PHP зібрано з libzip ≥ 1.7.0.

### Дивіться також

-   [ZipArchive::setCompressionIndex()](ziparchive.setcompressionindex.html) - Встановити метод стиснення запису, заданого його індексом
-   [ZipArchive::setCompressionName()](ziparchive.setcompressionname.html) - Встановити метод стиснення запису, заданого на ім'я