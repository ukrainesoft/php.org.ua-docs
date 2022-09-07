---
navigation:
  - streamwrapper.unlink.md: '« streamWrapper::unlink'
  - ref.stream.md: Функції для роботи з потоками »
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::urlстати'
---
# streamWrapper::urlстати

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::urlstat — Отримання інформації про файл

### Опис

```methodsynopsis
public streamWrapper::url_stat(string $path, int $flags): array|false
```

Цей метод викликається в процесі виконання будь-якої [stat()](function.stat.md) функцій, таких як:

-   [copy()](function.copy.md)
-   [fileperms()](function.fileperms.md)
-   [fileinode()](function.fileinode.md)
-   [filesize()](function.filesize.md)
-   [fileowner()](function.fileowner.md)
-   [filegroup()](function.filegroup.md)
-   [fileatime()](function.fileatime.md)
-   [filemtime()](function.filemtime.md)
-   [filectime()](function.filectime.md)
-   [filetype()](function.filetype.md)
-   [ісwritable()](function.is-writable.md)
-   [ісreadable()](function.is-readable.md)
-   [ісexecutable()](function.is-executable.md)
-   [ісfile()](function.is-file.md)
-   [ісdir()](function.is-dir.md)
-   [ісlink()](function.is-link.md)
-   [fileexists()](function.file-exists.md)
-   [lstat()](function.lstat.md)
-   [stat()](function.stat.md)
-   [SplFileInfo::getPerms()](splfileinfo.getperms.md)
-   [SplFileInfo::getInode()](splfileinfo.getinode.md)
-   [SplFileInfo::getSize()](splfileinfo.getsize.md)
-   [SplFileInfo::getOwner()](splfileinfo.getowner.md)
-   [SplFileInfo::getGroup()](splfileinfo.getgroup.md)
-   [SplFileInfo::getATime()](splfileinfo.getatime.md)
-   [SplFileInfo::getMTime()](splfileinfo.getmtime.md)
-   [SplFileInfo::getCTime()](splfileinfo.getctime.md)
-   [SplFileInfo::getType()](splfileinfo.gettype.md)
-   [SplFileInfo::isWritable()](splfileinfo.iswritable.md)
-   [SplFileInfo::isReadable()](splfileinfo.isreadable.md)
-   [SplFileInfo::isExecutable()](splfileinfo.isexecutable.md)
-   [SplFileInfo::isFile()](splfileinfo.isfile.md)
-   [SplFileInfo::isDir()](splfileinfo.isdir.md)
-   [SplFileInfo::isLink()](splfileinfo.islink.md)
-   [RecursiveDirectoryIterator::hasChildren()](recursivedirectoryiterator.haschildren.md)

### Список параметрів

`path`

Шлях до файлу чи його URL. Пам'ятайте, що URL-адреса повинна бути відокремлена символами :// , інші форми URL-адреси не підтримуються.

`flags`

Зберігає додаткові прапори, встановлені потоками API. Може зберігати одне або кілька нижченаведених значень, об'єднаних операцією АБО.

| Флаг | Описание |
| --- | --- |
| STREAMURLСТАТИLINK | Для ресурсів, які можуть посилатися на інші ресурси (наприклад, HTTP Location: forward, або символічні посилання файлової системи). Цей прапор вказує, що інформація, що повертається, відноситься до самого посилання, а не до ресурсу, на який вона вказує. Цей використовується під час виклику функцій [lstat()](function.lstat.md) [ісlink()](function.is-link.md) або [filetype()](function.filetype.md) |
| STREAMURLСТАТИQUIET | Якщо прапорець встановлений, обгортка не повинна викликати жодних помилок. Якщо ні, можна викликати повідомлення про помилки за допомогою функції [triggererror()](function.trigger-error.md) |

### Значення, що повертаються

Має повертатися масив (array) з тими самими елементами, що у [stat()](function.stat.md). Невідомі або недоступні значення необхідно призводити до розумних значень (зазвичай до **`0`**). Зверніть особливу увагу на `mode`, як описано в розділі [stat()](function.stat.md). У разі виникнення помилки повертає **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [stat()](function.stat.md) - Повертає інформацію про файл
-   [streamwrapper::streamstat()](streamwrapper.stream-stat.md) - Отримання інформації про файловий ресурс
