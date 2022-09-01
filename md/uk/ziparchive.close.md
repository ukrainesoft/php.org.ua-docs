---
navigation:
  - ziparchive.clearerror.md: '« ZipArchive::clearError'
  - ziparchive.count.md: 'ZipArchive::count »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::close'
---
# ZipArchive::close

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::close — Закриває активний архів (відкритий або знову створений)

### Опис

```methodsynopsis
public ZipArchive::close(): bool
```

Закриває відкритий або створений архів та зберігає зміни. Метод автоматично викликається наприкінці виконання сценарію.

Якщо архів не містить файлів, файл видаляється повністю (порожній архів не записується).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
