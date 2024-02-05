---
navigation:
  - rarentry.isdirectory.md: '« RarEntry::isDirectory'
  - rarentry.tostring.md: 'RarEntry::\_\_toString »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::isEncrypted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarEntry::isEncrypted

(PECL rar >= 2.0.0)

RarEntry::isEncrypted — Перевіряє, чи зашифрований запис

### Опис

```methodsynopsis
public RarEntry::isEncrypted(): bool
```

Перевіряє, чи зашифровано поточний запис.

> **Зауваження** :
> 
> В тому самому архіві для різних файлів можуть використовуватися різні паролі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`** або **`false`\*\*в зависимости от результата.
