---
navigation:
  - wrappers.http.md: '« http://'
  - wrappers.php.md: 'php:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'ftp://'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
-   ftps://user:[password@example.com](mailto:password@example.com)/pub/file.txt

### Опції

**Основна інформація**

| Атрибут | Поддерживается |
| --- | --- |
| Обмеження по [allow\_url\_fopen](filesystem.configuration.md#ini.allow-url-fopen) | Так |
| Читання | Так |
| Запис | Так (нові файли / існуючі файли з опцією `overwrite`) . |
| Додавання | Так |
| Одночасне читання та запис | Ні |
| Поддержка[stat()](function.stat.md) | [filesize()](function.filesize.md) [filemtime()](function.filemtime.md) [filetype()](function.filetype.md) [file\_exists()](function.file-exists.md) [is\_file()](function.is-file.md) і [is\_dir()](function.is-dir.md) |
| Поддержка[unlink()](function.unlink.md) | Так |
| Поддержка[rename()](function.rename.md) | Так |
| Поддержка[mkdir()](function.mkdir.md) | Так |
| Поддержка[rmdir()](function.rmdir.md) | Так |

### Примітки

> **Зауваження** :
> 
> FTPS поддерживается только тогда, когда включена поддержка модуля[OpenSSL](book.openssl.md)
> 
> Якщо сервер не підтримує SSL, з'єднання перемикається назад на звичайний нешифрований протокол FTP.

> **Зауваження** **Доповнення**  
> Файли можуть бути дописані за допомогою URL-обгортки `ftp://`

### Дивіться також

-   [Параметри контексту FTP](context.ftp.md)
