---
navigation:
  - rarentry.getcrc.md: '« RarEntry::getCrc'
  - rarentry.gethostos.md: 'RarEntry::getHostOs »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getFileTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Останнім часом повертає зміни елемента у вигляді рядка у форматі `YYYY-MM-DD HH:II:SS`, или\*\*`false`\*\*в случае возникновения ошибки.
