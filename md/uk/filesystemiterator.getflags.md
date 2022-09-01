---
navigation:
  - filesystemiterator.current.html: '« FilesystemIterator::current'
  - filesystemiterator.key.html: 'FilesystemIterator::key »'
  - index.html: PHP Manual
  - class.filesystemiterator.html: FilesystemIterator
title: 'FilesystemIterator::getFlags'
---
# FilesystemIterator::getFlags

(PHP 5> = 5.3.0, PHP 7, PHP 8)

FilesystemIterator::getFlags — Отримання прапорів налаштувань об'єкта

### Опис

```methodsynopsis
public FilesystemIterator::getFlags(): int
```

Отримує значення прапорів налаштувань об'єкта у вигляді, як вони були задані методами [FilesystemIterator::construct()](filesystemiterator.construct.html) або [FilesystemIterator::setFlags()](filesystemiterator.setflags.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ціле число, яке представляє задані прапори.

### Дивіться також

-   [FilesystemIterator::construct()](filesystemiterator.construct.html) - Створює новий ітератор файлової системи
-   [FilesystemIterator::setFlags()](filesystemiterator.setflags.html) - Завдання прапорів обробки
