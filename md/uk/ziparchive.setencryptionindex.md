Встановити метод шифрування запису за його індексом

-   [« ZipArchive::setCompressionName](ziparchive.setcompressionname.html)
    
-   [ZipArchive::setEncryptionName »](ziparchive.setencryptionname.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Встановити метод шифрування запису за його індексом
    

# ZipArchive::setEncryptionIndex

(PHP >= 7.2.0, PHP 8, PECL zip >= 1.14.0)

ZipArchive::setEncryptionIndex — Встановити метод шифрування запису за його індексом

### Опис

```methodsynopsis
public ZipArchive::setEncryptionIndex(int $index, int $method, ?string $password = null): bool
```

Встановлює метод шифрування запису, вказаного за індексом.

### Список параметрів

`index`

Індекс запису.

`method`

Метод шифрування, заданий однією із констант ZipArchive::EM

`password`

Пароль. Якщо не вказувати, буде використано пароль за замовчуванням.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `password` тепер допускає значення null. |

### Примітки

> **Зауваження**
> 
> Функція доступна лише якщо скомпільовано за допомогою libzip ≥ 1.2.0.

### Дивіться також

-   [ZipArchive::setPassword()](ziparchive.setpassword.html) - Встановлення пароля для активного архіву
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.html) - Встановити метод шифрування запису на його ім'я