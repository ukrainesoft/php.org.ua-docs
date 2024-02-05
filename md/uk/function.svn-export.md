---
navigation:
  - function.svn-diff.md: « svn\_diff
  - function.svn-fs-abort-txn.md: svn\_fs\_abort\_txn »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_export

(PECL svn >= 0.3.0)

svn\_export — Експортує вміст директорії SVN

### Опис

```methodsynopsis
svn_export(    string $frompath,    string $topath,    bool $working_copy = true,    int $revision_no = -1): bool
```

Експортує дані як з робочої копії, так і з репозиторію в чисту директорію.

### Список параметрів

`frompath`

Шлях до поточного репозиторію або робочої копії.

`topath`

Шлях до "чистої" папки для експорту.

`working_copy`

При\*\*`true`\*\* з робочої копії будуть також експортовані ненаправлені в репозиторій файли.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**svn\_export()\*\*\*\*

```php
<?php
$working_dir     = '../';
$new_working_dir = '/home/user/devel/foo/trunk';

svn_export($working_dir, $new_working_dir);
?>
```

### Дивіться також

-   [svn\_import()](function.svn-import.md) \- Імпорт шляху без версії до репозиторії
