---
navigation:
  - function.svn-repos-recover.md: « svnreposrecover
  - function.svn-status.md: svnstatus »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svnrevert
---
# svnrevert

(PECL svn >= 0.3.0)

svnrevert — Скасує локальні зміни робочої копії

### Опис

```methodsynopsis
svn_revert(string $path, bool $recursive = false): bool
```

Скасує всі локальні зміни файлів, розміщених у робочій копії.

### Список параметрів

`path`

Шлях до робочої копії.

`recursive`

Опціональний параметр рекурсивного скасування правок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [svndelete()](function.svn-delete.md) - Видаляє елементи з робочої копії або репозиторію
-   [svnexport()](function.svn-export.md) - Експортує вміст директорії SVN
