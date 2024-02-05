---
navigation:
  - rarentry.getattr.md: '« RarEntry::getAttr'
  - rarentry.getfiletime.md: 'RarEntry::getFileTime »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::getCrc'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarEntry::getCrc

(PECL rar >= 0.1)

RarEntry::getCrc — Повертає CRC елемент архіву

### Опис

```methodsynopsis
public RarEntry::getCrc(): string
```

Повертає шістнадцяткове рядкове представлення CRC елемента архіву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає CRC елемента архіву або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL rar 2.0.0 | Тепер цей метод повертає коректні значення багатотомних архівів. |
