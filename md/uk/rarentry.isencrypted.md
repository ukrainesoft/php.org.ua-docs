---
navigation:
  - rarentry.isdirectory.md: '« RarEntry::isDirectory'
  - rarentry.tostring.md: 'RarEntry::toString »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::isEncrypted'
---
# RarEntry::isEncrypted

(PECL rar >= 2.0.0)

RarEntry::isEncrypted — Перевіряє, чи зашифрований запис

### Опис

```methodsynopsis
public RarEntry::isEncrypted(): bool
```

Перевіряє, чи зашифровано поточний запис.

> **Зауваження**
> 
> В тому самому архіві для різних файлів можуть використовуватися різні паролі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`** Залежно від результату.
