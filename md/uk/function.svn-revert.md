---
navigation:
  - function.svn-repos-recover.md: « svn\_repos\_recover
  - function.svn-status.md: svn\_status »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_revert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_revert

(PECL svn >= 0.3.0)

svn\_revert — Скасує локальні зміни робочої копії

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [svn\_delete()](function.svn-delete.md) \- Видаляє елементи з робочої копії або репозиторію
-   [svn\_export()](function.svn-export.md) \- Експортує вміст директорії SVN
