---
navigation:
  - function.svn-ls.md: « svn\_ls
  - function.svn-repos-create.md: svn\_repos\_create »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_mkdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_mkdir

(PECL svn >= 0.4.0)

svn\_mkdir — Створює директорію в робочій копії або репозиторії

### Опис

```methodsynopsis
svn_mkdir(string $path, string $log_message = ?): bool
```

Створює директорію у робочій копії чи репозиторії.

### Список параметрів

`path`

Шлях до робочої копії чи репозиторію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [svn\_add()](function.svn-add.md) \- Додає елементи до списку запланованих для додавання до робочої копії
-   **svn\_copy()**
