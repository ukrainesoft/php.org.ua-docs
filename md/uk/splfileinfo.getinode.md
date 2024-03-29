---
navigation:
  - splfileinfo.getgroup.md: '« SplFileInfo::getGroup'
  - splfileinfo.getlinktarget.md: 'SplFileInfo::getLinkTarget »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getInode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getInode

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getInode — Отримує індексний дескриптор для файлу

### Опис

```methodsynopsis
public SplFileInfo::getInode(): int|false
```

Отримує номер індексного дескриптора об'єкта файлової системи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер індексного дескриптора для об'єкта файлової системи у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі виникнення помилки викидає виняток [RuntimeException](class.runtimeexception.md)

### Дивіться також

-   [fileinode()](function.fileinode.md) \- Повертає індексний дескриптор файлу
