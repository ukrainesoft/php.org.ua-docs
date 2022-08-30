Доступ до URL-адрес за протоколом FTP(s)

-   [http://](wrappers.http.html)
    
-   [php:// »](wrappers.php.html)
    
-   [PHP Manual](index.html)
    
-   [Підтримувані протоколи та обгортки](wrappers.html)
    
-   Доступ до URL-адрес за протоколом FTP(s)
    

# ftp://

# ftps://

ftp:// -- ftps:// — Доступ до URL-адрес за протоколом FTP(s)

### Опис

Дозволяє читати існуючі файли та створювати нові файли через FTP. Якщо FTP-сервер не підтримує пасивний режим, з'єднання буде неможливо.

Ви можете відкрити файл або для читання або для запису, але не одночасно для того й іншого. Якщо файл на сервері FTP вже існує, і ви намагаєтеся відкрити його для запису, але не вказали опцію контексту `overwrite`, з'єднання буде неможливо. Якщо вам потрібно перезаписати існуючі файли на FTP, вкажіть опцію `overwrite` у контексті та відкрийте файл для запису. Крім того, ви можете використовувати [модуль FTP](ref.ftp.html)

Якщо ви встановили директиву [from](filesystem.configuration.html#ini.from) у файлі php.ini, це значення буде відправлено як пароль при анонімному підключенні до FTP.

### Використання

-   [ftp://example.com/pub/file.txt](ftp://example.com/pub/file.txt)
-   [ftp://user:password@example.com/pub/file.txt](ftp://user:password@example.com/pub/file.txt)
-   ftps://example.com/pub/file.txt
-   ftps://user:[password@example.com](mailto:password@example.com)/пуб/філе.тхт

### Опції

**Основна інформація**

| Атрибут                                                                         | Поддерживается                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Обмеження по [allowurlfopen](filesystem.configuration.html#ini.allow-url-fopen) | Так                                                                                                                                                                                                                            |
| Читання                                                                         | Так                                                                                                                                                                                                                            |
| Запис                                                                           | Так (нові файли / існуючі файли з опцією `overwrite`                                                                                                                                                                           |
| Додавання                                                                       | Так                                                                                                                                                                                                                            |
| Одночасне читання та запис                                                      | Ні                                                                                                                                                                                                                             |
| Підтримка [stat()](function.stat.html)                                          | [filesize()](function.filesize.html) [filemtime()](function.filemtime.html) [filetype()](function.filetype.html) [fileexists()](function.file-exists.html) [ісfile()](function.is-file.html) і [ісdir()](function.is-dir.html) |
| Підтримка [unlink()](function.unlink.html)                                      | Так                                                                                                                                                                                                                            |
| Підтримка [rename()](function.rename.html)                                      | Так                                                                                                                                                                                                                            |
| Підтримка [mkdir()](function.mkdir.html)                                        | Так                                                                                                                                                                                                                            |
| Підтримка [rmdir()](function.rmdir.html)                                        | Так                                                                                                                                                                                                                            |

### Примітки

> **Зауваження**
> 
> FTPS підтримується лише тоді, коли увімкнена підтримка модуля [OpenSSL](book.openssl.html)
> 
> Якщо сервер не підтримує SSL, з'єднання перемикається назад на звичайний нешифрований протокол FTP.

> **Зауваження** **Доповнення**  
> Файли можуть бути дописані за допомогою URL-обгортки `ftp://`

### Дивіться також

-   [Параметри контексту FTP](context.ftp.html)