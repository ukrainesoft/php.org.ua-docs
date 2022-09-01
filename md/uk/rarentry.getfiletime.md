---
navigation:
  - rarentry.getcrc.html: '« RarEntry::getCrc'
  - rarentry.gethostos.html: 'RarEntry::getHostOs »'
  - index.html: PHP Manual
  - class.rarentry.html: RarEntry
title: 'RarEntry::getFileTime'
---
# RarEntry::getFileTime

(PECL rar >= 0.1)

RarEntry::getFileTime — Повертає останнім часом зміни елемента

### Опис

```methodsynopsis
public RarEntry::getFileTime(): string
```

Останнім часом повертає зміни елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнім часом повертає зміни елемента у вигляді рядка у форматі `YYYY-MM-DD HH:II:SS`, або **`false`** у разі виникнення помилки.
