---
navigation:
  - class.phar.md: « Phar
  - phar.addfile.md: 'Phar::addFile »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::addEmptyDir'
---
# Phar::addEmptyDir

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::addEmptyDir — Додає в phar-архів порожню директорію

### Опис

```methodsynopsis
public Phar::addEmptyDir(string $directory): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

За допомогою цього методу створюється порожня директорія, шлях до якої вказано `dirname`. Цей метод аналогічний [ZipArchive::addEmptyDir()](ziparchive.addemptydir.md)

### Список параметрів

`directory`

Ім'я порожнього каталогу, який має бути створений у phar-архіві.

### Значення, що повертаються

Немає значення, що повертається, у разі виникнення помилки викидається виняток.

### Приклади

**Приклад #1 Приклад використання **Phar::addEmptyDir()****

```php
<?php
try {
    $a = new Phar('/путь/к/phar.phar');

    $a->addEmptyDir('/полный/путь/к/файлу');
    // показывает, как хранится этот файл
    $b = $a['полный/путь/к/файлу']->isDir();
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [PharData::addEmptyDir()](phardata.addemptydir.md) - Додати порожню директорію до tar/zip-архіву
-   [Phar::addFile()](phar.addfile.md) - Додає в phar-архів файл із файлової системи
-   [Phar::addFromString()](phar.addfromstring.md) - Додає в phar-архів файл із рядка
