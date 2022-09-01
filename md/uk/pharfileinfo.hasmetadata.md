---
navigation:
  - pharfileinfo.getpharflags.md: '« PharFileInfo::getPharFlags'
  - pharfileinfo.iscrcchecked.md: 'PharFileInfo::isCRCChecked »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::hasMetadata'
---
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

-   [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.md) - Встановлення метаданих для конкретного файлу
-   [PharFileInfo::getMetadata()](pharfileinfo.getmetadata.md) - Отримати метадані, пов'язані з файлом
-   [PharFileInfo::delMetadata()](pharfileinfo.delmetadata.md) - Видалити метадані файлу
-   [Phar::setMetadata()](phar.setmetadata.md) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.md) - Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.md) - Витягти метадані phar-архіву
