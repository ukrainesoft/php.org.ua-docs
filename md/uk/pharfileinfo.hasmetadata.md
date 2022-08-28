Перевірити, чи є у файлу метадані

-   [« PharFileInfo::getPharFlags](pharfileinfo.getpharflags.html)
    
-   [PharFileInfo::isCRCChecked »](pharfileinfo.iscrcchecked.html)
    
-   [PHP Manual](index.html)
    
-   [PharFileInfo](class.pharfileinfo.html)
    
-   Перевірити, чи є у файлу метадані
    

# PharFileInfo::hasMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

PharFileInfo::hasMetadata — Перевірити, чи є у файлу метадані

### Опис

```methodsynopsis
public PharFileInfo::hasMetadata(): bool
```

Перевіряє, чи є файли метадані.

### Список параметрів

Немає параметрів.

### Значення, що повертаються

Повертає **`false`** або **`true`** (метадані, рівні **`null`**, вважаються за відсутність метаданих)

### Дивіться також

-   [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.html) - Встановлення метаданих для конкретного файлу
-   [PharFileInfo::getMetadata()](pharfileinfo.getmetadata.html) - Отримати метадані, пов'язані з файлом
-   [PharFileInfo::delMetadata()](pharfileinfo.delmetadata.html) - Видалити метадані файлу
-   [Phar::setMetadata()](phar.setmetadata.html) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.html) - Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.html) - Витягти метадані phar-архіву