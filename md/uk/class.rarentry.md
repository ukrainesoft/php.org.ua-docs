Клас RarEntry

-   [« RarArchive::toString](rararchive.tostring.md)
    
-   [RarEntry::extract »](rarentry.extract.md)
    
-   [PHP Manual](index.md)
    
-   [Rar](book.rar.md)
    
-   Клас RarEntry
    

# Клас [RarEntry](class.rarentry.md)

(PECL rar >= 0.1)

## Вступ

Запис RAR, який представляє директорію або стислий файл усередині архіву RAR.

## Огляд класів

```classsynopsis



    
     
      final
      class RarEntry
     
     {

    /* Константы */
    
     const
     int
      HOST_MSDOS = 0;

    const
     int
      HOST_OS2 = 1;

    const
     int
      HOST_WIN32 = 2;

    const
     int
      HOST_UNIX = 3;

    const
     int
      HOST_MACOS = 4;

    const
     int
      HOST_BEOS = 5;

    const
     int
      ATTRIBUTE_WIN_READONLY = 1;

    const
     int
      ATTRIBUTE_WIN_HIDDEN = 2;

    const
     int
      ATTRIBUTE_WIN_SYSTEM = 4;

    const
     int
      ATTRIBUTE_WIN_DIRECTORY = 16;

    const
     int
      ATTRIBUTE_WIN_ARCHIVE = 32;

    const
     int
      ATTRIBUTE_WIN_DEVICE = 64;

    const
     int
      ATTRIBUTE_WIN_NORMAL = 128;

    const
     int
      ATTRIBUTE_WIN_TEMPORARY = 256;

    const
     int
      ATTRIBUTE_WIN_SPARSE_FILE = 512;

    const
     int
      ATTRIBUTE_WIN_REPARSE_POINT = 1024;

    const
     int
      ATTRIBUTE_WIN_COMPRESSED = 2048;

    const
     int
      ATTRIBUTE_WIN_OFFLINE = 4096;

    const
     int
      ATTRIBUTE_WIN_NOT_CONTENT_INDEXED = 8192;

    const
     int
      ATTRIBUTE_WIN_ENCRYPTED = 16384;

    const
     int
      ATTRIBUTE_WIN_VIRTUAL = 65536;

    const
     int
      ATTRIBUTE_UNIX_WORLD_EXECUTE = 1;

    const
     int
      ATTRIBUTE_UNIX_WORLD_WRITE = 2;

    const
     int
      ATTRIBUTE_UNIX_WORLD_READ = 4;

    const
     int
      ATTRIBUTE_UNIX_GROUP_EXECUTE = 8;

    const
     int
      ATTRIBUTE_UNIX_GROUP_WRITE = 16;

    const
     int
      ATTRIBUTE_UNIX_GROUP_READ = 32;

    const
     int
      ATTRIBUTE_UNIX_OWNER_EXECUTE = 64;

    const
     int
      ATTRIBUTE_UNIX_OWNER_WRITE = 128;

    const
     int
      ATTRIBUTE_UNIX_OWNER_READ = 256;

    const
     int
      ATTRIBUTE_UNIX_STICKY = 512;

    const
     int
      ATTRIBUTE_UNIX_SETGID = 1024;

    const
     int
      ATTRIBUTE_UNIX_SETUID = 2048;

    const
     int
      ATTRIBUTE_UNIX_FINAL_QUARTET = 61440;

    const
     int
      ATTRIBUTE_UNIX_FIFO = 4096;

    const
     int
      ATTRIBUTE_UNIX_CHAR_DEV = 8192;

    const
     int
      ATTRIBUTE_UNIX_DIRECTORY = 16384;

    const
     int
      ATTRIBUTE_UNIX_BLOCK_DEV = 24576;

    const
     int
      ATTRIBUTE_UNIX_REGULAR_FILE = 32768;

    const
     int
      ATTRIBUTE_UNIX_SYM_LINK = 40960;

    const
     int
      ATTRIBUTE_UNIX_SOCKET = 49152;


    /* Методы */
    
   public extract(    string $dir,    string $filepath = "",    string $password = NULL,    bool $extended_data = false): bool
public getAttr(): int
public getCrc(): string
public getFileTime(): string
public getHostOs(): int
public getMethod(): int
public getName(): string
public getPackedSize(): int
public getStream(string $password = ?): resource|false
public getUnpackedSize(): int
public getVersion(): int
public isDirectory(): bool
public isEncrypted(): bool
public __toString(): string

   }
```

## Обумовлені константи

**`RarEntry::HOST_MSDOS`**

Якщо повернене значення [RarEntry::getHostOs()](rarentry.gethostos.md) і цієї константі, отже цей запис було додано в MS-DOS. Введено для заміни **`RAR_HOST_MSDOS`**

**`RarEntry::HOST_OS2`**

Якщо повернене значення [RarEntry::getHostOs()](rarentry.gethostos.md) і цієї константі, отже цей запис було додано в OS/2. Введено для заміни **`RAR_HOST_OS2`**

**`RarEntry::HOST_WIN32`**

Якщо повернене значення [RarEntry::getHostOs()](rarentry.gethostos.md) і цієї константі, отже цей запис було додано до Microsoft Windows. Введено для заміни **`RAR_HOST_WIN32`**

**`RarEntry::HOST_UNIX`**

Якщо повернене значення [RarEntry::getHostOs()](rarentry.gethostos.md) і цієї константі, отже цей запис було додано в UNIX. Введено для заміни **`RAR_HOST_UNIX`**

**`RarEntry::HOST_MACOS`**

Якщо повернене значення [RarEntry::getHostOs()](rarentry.gethostos.md) і цієї константі, отже цей запис було додано до Mac OS.

**`RarEntry::HOST_BEOS`**

Якщо повернене значення [RarEntry::getHostOs()](rarentry.gethostos.md) і цієї константі, отже цей запис було додано до BeOS. Введено для заміни **`RAR_HOST_BEOS`**

**`RarEntry::ATTRIBUTE_WIN_READONLY`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "read-only" для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_HIDDEN`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "hidden" для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_SYSTEM`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "system" для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_DIRECTORY`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "directory" (є директорією) для записів Windows. Також дивіться опис методу [RarEntry::isDirectory()](rarentry.isdirectory.md), який також працює із записами, доданими не через WinRAR.

**`RarEntry::ATTRIBUTE_WIN_ARCHIVE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "archive" для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_DEVICE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "device" для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_NORMAL`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "normal file" (НЕ є директорією) для записів Windows. Також дивіться опис методу [RarEntry::isDirectory()](rarentry.isdirectory.md), який також працює із записами, доданими не через WinRAR.

**`RarEntry::ATTRIBUTE_WIN_TEMPORARY`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "temporary" для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_SPARSE_FILE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "sparse file" (розріджений файл NTFS) для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_REPARSE_POINT`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис з атрибутом "reparse point" (файл точки повторної обробки NTFS, тобто перетин директорій або точка монтування файлової системи) для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_COMPRESSED`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис із атрибутом "compressed" (тільки NTFS) для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_OFFLINE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "offline" (запис вимкнений і недоступний) для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_NOT_CONTENT_INDEXED`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "not content indexed" (запис має бути проіндексований) для записів Windows.

**`RarEntry::ATTRIBUTE_WIN_ENCRYPTED`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "encrypted" (тільки NTFS) для Windows.

**`RarEntry::ATTRIBUTE_WIN_VIRTUAL`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "virtual" (тільки NTFS) для Windows.

**`RarEntry::ATTRIBUTE_UNIX_WORLD_EXECUTE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис з атрибутом "executable" для всіх для UNIX записів.

**`RarEntry::ATTRIBUTE_UNIX_WORLD_WRITE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "writable" для всіх для UNIX записів.

**`RarEntry::ATTRIBUTE_UNIX_WORLD_READ`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "readable" для всіх для UNIX записів.

**`RarEntry::ATTRIBUTE_UNIX_GROUP_EXECUTE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис із атрибутом "executable" для групи для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_GROUP_WRITE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис із атрибутом "writable" для групи для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_GROUP_READ`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "readable" для групи для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_OWNER_EXECUTE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, який представляє запис з атрибутом "executable" для власника для UNIX записів.

**`RarEntry::ATTRIBUTE_UNIX_OWNER_WRITE`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "writable" для власника для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_OWNER_READ`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із атрибутом "readable" для власника для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_STICKY`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із встановленим "sticky bit" для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_SETGID`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із встановленим "setgid" для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_SETUID`**

Використовується з [RarEntry::getAttr()](rarentry.getattr.md). Біт, що представляє запис із встановленим "setuid" для записів UNIX.

**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**

Маска для ізоляції чотирьох останніх біт (напівбайт) для атрибутів UNIX (ЗIFMT, тип файлової маски). Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константами [**`RarEntry::ATTRIBUTE_UNIX_FIFO`**](class.rarentry.html#rarentry.constants.attribute-unix-fifo) [**`RarEntry::ATTRIBUTE_UNIX_CHAR_DEV`**](class.rarentry.html#rarentry.constants.attribute-unix-char-dev) [**`RarEntry::ATTRIBUTE_UNIX_DIRECTORY`**](class.rarentry.html#rarentry.constants.attribute-unix-directory) [**`RarEntry::ATTRIBUTE_UNIX_BLOCK_DEV`**](class.rarentry.html#rarentry.constants.attribute-unix-block-dev) [**`RarEntry::ATTRIBUTE_UNIX_REGULAR_FILE`**](class.rarentry.html#rarentry.constants.attribute-unix-regular-file) [**`RarEntry::ATTRIBUTE_UNIX_SYM_LINK`**](class.rarentry.html#rarentry.constants.attribute-unix-sym-link) і [**`RarEntry::ATTRIBUTE_UNIX_SOCKET`**](class.rarentry.html#rarentry.constants.attribute-unix-socket)

**`RarEntry::ATTRIBUTE_UNIX_FIFO`**

Спеціальні файли FIFO в Unix матимуть це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet)

**`RarEntry::ATTRIBUTE_UNIX_CHAR_DEV`**

Спеціальні файли символьних пристроїв у Unix будуть мати це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet)

**`RarEntry::ATTRIBUTE_UNIX_DIRECTORY`**

Директорії в Unix матимуть це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet). Також дивіться опис методу [RarEntry::isDirectory()](rarentry.isdirectory.md), який також працює із записами доданими в інших операційних системах.

**`RarEntry::ATTRIBUTE_UNIX_BLOCK_DEV`**

Спеціальні файли блокових пристроїв у Unix будуть мати це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet)

**`RarEntry::ATTRIBUTE_UNIX_REGULAR_FILE`**

Звичайні файли (не директорії) у Unix матимуть це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet). Також дивіться опис методу [RarEntry::isDirectory()](rarentry.isdirectory.md), який також працює із записами доданими в інших операційних системах.

**`RarEntry::ATTRIBUTE_UNIX_SYM_LINK`**

Символічні посилання в Unix матимуть це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet)

**`RarEntry::ATTRIBUTE_UNIX_SOCKET`**

Спеціальні файли сокетів у Unix матимуть це значення у чотирьох останніх бітах. Використовується з [RarEntry::getAttr()](rarentry.getattr.md) та константою [**`RarEntry::ATTRIBUTE_UNIX_FINAL_QUARTET`**](class.rarentry.html#rarentry.constants.attribute-unix-final-quartet)

## Зміст

-   [RarEntry::extract](rarentry.extract.md) — Витягує елемент із архіву
-   [RarEntry::getAttr](rarentry.getattr.md) — Повертає атрибути елемента архіву
-   [RarEntry::getCrc](rarentry.getcrc.md) — Повертає CRC елемент архіву
-   [RarEntry::getFileTime](rarentry.getfiletime.md) — Останнім часом повертає зміни елемента
-   [RarEntry::getHostOs](rarentry.gethostos.md) — Повертає оригінальну ОС елемента
-   [RarEntry::getMethod](rarentry.getmethod.md) — Повертає метод компресії елемента
-   [RarEntry::getName](rarentry.getname.md) — Повертає ім'я елемента
-   [RarEntry::getPackedSize](rarentry.getpackedsize.md) — Повертає розмір стисненого елемента
-   [RarEntry::getStream](rarentry.getstream.md) — Отримати обробник для запису
-   [RarEntry::getUnpackedSize](rarentry.getunpackedsize.md) — Повертає розмір елемента у розпакованому стані
-   [RarEntry::getVersion](rarentry.getversion.md) — Повертає мінімальну версію програми RAR, необхідну для розпакування елемента
-   [RarEntry::isDirectory](rarentry.isdirectory.md) — Перевіряє, чи є запис директорією
-   [RarEntry::isEncrypted](rarentry.isencrypted.md) — Перевіряє, чи зашифрований запис
-   [RarEntry::toString](rarentry.tostring.md) — Отримати текстове подання запису