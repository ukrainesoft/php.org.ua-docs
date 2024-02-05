---
navigation:
  - streamwrapper.unlink.md: '« streamWrapper::unlink'
  - ref.stream.md: Функції для роботи з потоками »
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::url\_stat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::url\_stat

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::url\_stat — Отримання інформації про файл

### Опис

```methodsynopsis
public streamWrapper::url_stat(string $path, int $flags): array|false
```

Цей метод викликається в процесі виконання будь-якої [stat()](function.stat.md)функций, таких как:

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
-   [is\_writable()](function.is-writable.md)
-   [is\_readable()](function.is-readable.md)
-   [is\_executable()](function.is-executable.md)
-   [is\_file()](function.is-file.md)
-   [is\_dir()](function.is-dir.md)
-   [is\_link()](function.is-link.md)
-   [file\_exists()](function.file-exists.md)
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

Шлях до файлу або його URL-адреси. Пам'ятайте, що URL-адреса повинна бути відокремлена символами :// , інші форми URL-адреси не підтримуються.

`flags`

Зберігає додаткові прапори, встановлені потоками API. Може зберігати одне або кілька нижченаведених значень, об'єднаних операцією АБО.

| Флаг | Опис |
| --- | --- |
| STREAM\_URL\_STAT\_LINK | Для ресурсів, які можуть посилатися на інші ресурси (наприклад, HTTP Location: forward, або символічні посилання файлової системи). Цей прапор вказує, що інформація, що повертається, відноситься до самого посилання, а не до ресурсу, на який вона вказує. Цей використовується під час виклику функцій [lstat()](function.lstat.md) [is\_link()](function.is-link.md) або [filetype()](function.filetype.md) |
| STREAM\_URL\_STAT\_QUIET | Якщо прапорець встановлений, обгортка не повинна викликати жодних помилок. Якщо ні, можна викликати повідомлення про помилки за допомогою функції [trigger\_error()](function.trigger-error.md) |

### Значення, що повертаються

Має повертатися масив (array) з тими самими елементами, що у [stat()](function.stat.md). Невідомі або недоступні значення необхідно призводити до розумних значень (зазвичай до ). Обратите особое внимание на`mode`, як описано в розділі [stat()](function.stat.md). У разі виникнення помилки повертає **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження** :
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [stat()](function.stat.md) \- Повертає інформацію про файл
-   [streamwrapper::stream\_stat()](streamwrapper.stream-stat.md) \- Отримання інформації про файловий ресурс
