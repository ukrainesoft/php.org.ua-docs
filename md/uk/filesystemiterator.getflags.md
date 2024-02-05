---
navigation:
  - filesystemiterator.current.md: '« FilesystemIterator::current'
  - filesystemiterator.key.md: 'FilesystemIterator::key »'
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::getFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FilesystemIterator::getFlags

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

FilesystemIterator::getFlags — Отримання прапорів налаштувань об'єкта

### Опис

```methodsynopsis
public FilesystemIterator::getFlags(): int
```

Отримує значення прапорів налаштувань об'єкта у вигляді, як вони були задані методами [FilesystemIterator::\_\_construct()](filesystemiterator.construct.md) або [FilesystemIterator::setFlags()](filesystemiterator.setflags.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ціле число, яке представляє задані прапори.

### Дивіться також

-   [FilesystemIterator::\_\_construct()](filesystemiterator.construct.md) \- Створює новий ітератор файлової системи
-   [FilesystemIterator::setFlags()](filesystemiterator.setflags.md) \- Завдання прапорів обробки
