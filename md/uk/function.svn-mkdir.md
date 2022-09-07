---
navigation:
  - function.svn-ls.md: « svnлс
  - function.svn-repos-create.md: svnreposcreate »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svnmkdir
---
# svnmkdir

(PECL svn >= 0.4.0)

svnmkdir — Створює директорію в робочій копії або репозиторії

### Опис

```methodsynopsis
svn_mkdir(string $path, string $log_message = ?): bool
```

Створює директорію у робочій копії чи репозиторії.

### Список параметрів

`path`

Шлях до робочої копії чи репозиторію.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [svnadd()](function.svn-add.md) - Додає елементи до списку запланованих для додавання до робочої копії
-   **svncopy()**
