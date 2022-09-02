---
navigation:
  - pharfileinfo.decompress.md: '« PharFileInfo::decompress'
  - pharfileinfo.destruct.md: 'PharFileInfo::destruct »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::delMetadata'
---
# PharFileInfo::delMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

PharFileInfo::delMetadata — Видалити метадані файлу

### Опис

```methodsynopsis
public PharFileInfo::delMetadata(): bool
```

Видаляє метадані файлу, якщо вони є.

### Список параметрів

Немає параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`** залежно від успішності виконання. Так як ця функціональність змінює phar-архів, необхідно, щоб опція [phar.readonly](phar.configuration.md#ini.phar.readonly) було відключено, інакше внести зміни до архіву [Phar](class.phar.md) не вийде. На архіви [PharData](class.phardata.md) обмеження на запис не поширюється.

### Помилки

Викидає виняток [PharException](class.pharexception.md) у разі виникнення помилки запису на диск, та [BadMethodCallException](class.badmethodcallexception.md), якщо запис заборонено.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::delMetaData()****

```php
<?php
try {
    $a = new Phar('myphar.phar');
    $a['hi'] = 'hi';
    var_dump($a['hi']->delMetadata());
    $a['hi']->setMetadata('there');
    var_dump($a['hi']->delMetadata());
    var_dump($a['hi']->delMetadata());
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.md) - Встановлення метаданих для конкретного файлу
-   [PharFileInfo::hasMetadata()](pharfileinfo.hasmetadata.md) - Перевірити, чи є у файлу метадані
-   [PharFileInfo::getMetadata()](pharfileinfo.getmetadata.md) - Отримати метадані, пов'язані з файлом
-   [Phar::setMetadata()](phar.setmetadata.md) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.md) - Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.md) - Витягти метадані phar-архіву
