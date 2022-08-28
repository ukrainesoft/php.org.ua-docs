Отримання інформації про файл

-   [« streamWrapper::unlink](streamwrapper.unlink.html)
    
-   [Функции для работы с потоками »](ref.stream.html)
    
-   [PHP Manual](index.html)
    
-   [streamWrapper](class.streamwrapper.html)
    
-   Отримання інформації про файл
    

# streamWrapper::urlстати

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::urlstat — Отримання інформації про файл

### Опис

```methodsynopsis
public streamWrapper::url_stat(string $path, int $flags): array|false
```

Цей метод викликається в процесі виконання будь-якої [stat()](function.stat.html) функцій, таких як:

-   [copy()](function.copy.html)
-   [fileperms()](function.fileperms.html)
-   [fileinode()](function.fileinode.html)
-   [filesize()](function.filesize.html)
-   [fileowner()](function.fileowner.html)
-   [filegroup()](function.filegroup.html)
-   [fileatime()](function.fileatime.html)
-   [filemtime()](function.filemtime.html)
-   [filectime()](function.filectime.html)
-   [filetype()](function.filetype.html)
-   [is\_writable()](function.is-writable.html)
-   [is\_readable()](function.is-readable.html)
-   [is\_executable()](function.is-executable.html)
-   [is\_file()](function.is-file.html)
-   [is\_dir()](function.is-dir.html)
-   [is\_link()](function.is-link.html)
-   [file\_exists()](function.file-exists.html)
-   [lstat()](function.lstat.html)
-   [stat()](function.stat.html)
-   [SplFileInfo::getPerms()](splfileinfo.getperms.html)
-   [SplFileInfo::getInode()](splfileinfo.getinode.html)
-   [SplFileInfo::getSize()](splfileinfo.getsize.html)
-   [SplFileInfo::getOwner()](splfileinfo.getowner.html)
-   [SplFileInfo::getGroup()](splfileinfo.getgroup.html)
-   [SplFileInfo::getATime()](splfileinfo.getatime.html)
-   [SplFileInfo::getMTime()](splfileinfo.getmtime.html)
-   [SplFileInfo::getCTime()](splfileinfo.getctime.html)
-   [SplFileInfo::getType()](splfileinfo.gettype.html)
-   [SplFileInfo::isWritable()](splfileinfo.iswritable.html)
-   [SplFileInfo::isReadable()](splfileinfo.isreadable.html)
-   [SplFileInfo::isExecutable()](splfileinfo.isexecutable.html)
-   [SplFileInfo::isFile()](splfileinfo.isfile.html)
-   [SplFileInfo::isDir()](splfileinfo.isdir.html)
-   [SplFileInfo::isLink()](splfileinfo.islink.html)
-   [RecursiveDirectoryIterator::hasChildren()](recursivedirectoryiterator.haschildren.html)

### Список параметрів

`path`

Шлях до файлу чи його URL. Пам'ятайте, що URL-адреса повинна бути відокремлена символами :// , інші форми URL-адреси не підтримуються.

`flags`

Зберігає додаткові прапори, встановлені потоками API. Може зберігати одне або кілька нижченаведених значень, об'єднаних операцією АБО.

| Флаг | Описание |
| --- | --- |
| STREAMURLСТАТИLINK | Для ресурсів, які можуть посилатися на інші ресурси (наприклад, HTTP Location: forward, або символічні посилання файлової системи). Цей прапор вказує, що інформація, що повертається, відноситься до самого посилання, а не до ресурсу, на який вона вказує. Цей використовується під час виклику функцій [lstat()](function.lstat.html) [is\_link()](function.is-link.html) або [filetype()](function.filetype.html) |
| STREAMURLСТАТИQUIET | Якщо прапорець встановлений, обгортка не повинна викликати жодних помилок. Якщо ні, можна викликати повідомлення про помилки за допомогою функції [trigger\_error()](function.trigger-error.html) |

### Значення, що повертаються

Має повертатися масив (array) з тими самими елементами, що у [stat()](function.stat.html). Невідомі або недоступні значення необхідно призводити до розумних значень (зазвичай до **`0`**). Зверніть особливу увагу на `mode`, як описано в розділі [stat()](function.stat.html). У разі виникнення помилки повертає **`false`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [stat()](function.stat.html) - Повертає інформацію про файл
-   [streamwrapper::stream\_stat()](streamwrapper.stream-stat.html) - Отримання інформації про файловий ресурс