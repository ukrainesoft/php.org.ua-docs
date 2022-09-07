---
navigation:
  - wrappers.http.md: 'http://'
  - wrappers.php.md: 'php:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'ftp://'
---
# ftp://

# ftps://

ftp:// -- ftps:// — Доступ до URL-адрес за протоколом FTP(s)

### Опис

Дозволяє читати існуючі файли та створювати нові файли через FTP. Якщо FTP-сервер не підтримує пасивний режим, з'єднання буде неможливо.

Ви можете відкрити файл або для читання або для запису, але не одночасно для того й іншого. Якщо файл на сервері FTP вже існує, і ви намагаєтеся відкрити його для запису, але не вказали опцію контексту `overwrite`, з'єднання буде неможливо. Якщо вам потрібно перезаписати існуючі файли на FTP, вкажіть опцію `overwrite` у контексті та відкрийте файл для запису. Крім того, ви можете використовувати [модуль FTP](ref.ftp.md)

Якщо ви встановили директиву [from](filesystem.configuration.md#ini.from) у файлі php.ini, це значення буде відправлено як пароль при анонімному підключенні до FTP.

### Використання

-   [ftp://example.com/pub/file.txt](ftp://example.com/pub/file.txt)
-   [ftp://user:password@example.com/pub/file.txt](ftp://user:password@example.com/pub/file.txt)
-   ftps://example.com/pub/file.txt
-   ftps://user:[password@example.com](mailto:password@example.com)/пуб/філе.тхт

### Опції

**Основна інформація**

| Атрибут | Поддерживается |
| --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | Так |
| Читання | Так |
| Запис | Так (нові файли / існуючі файли з опцією `overwrite` |
| Додавання | Так |
| Одночасне читання та запис | Ні |
| Підтримка [stat()](function.stat.md) | [filesize()](function.filesize.md) [filemtime()](function.filemtime.md) [filetype()](function.filetype.md) [fileexists()](function.file-exists.md) [ісfile()](function.is-file.md) і [ісdir()](function.is-dir.md) |
| Підтримка [unlink()](function.unlink.md) | Так |
| Підтримка [rename()](function.rename.md) | Так |
| Підтримка [mkdir()](function.mkdir.md) | Так |
| Підтримка [rmdir()](function.rmdir.md) | Так |

### Примітки

> **Зауваження**
> 
> FTPS підтримується лише тоді, коли увімкнена підтримка модуля [OpenSSL](book.openssl.md)
> 
> Якщо сервер не підтримує SSL, з'єднання перемикається назад на звичайний нешифрований протокол FTP.

> **Зауваження** **Доповнення**  
> Файли можуть бути дописані за допомогою URL-обгортки `ftp://`

### Дивіться також

-   [Параметри контексту FTP](context.ftp.md)
