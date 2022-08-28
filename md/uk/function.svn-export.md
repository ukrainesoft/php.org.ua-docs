Експортує вміст директорії SVN

-   [« svn\_diff](function.svn-diff.html)
    
-   [svn\_fs\_abort\_txn »](function.svn-fs-abort-txn.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SVN](ref.svn.html)
    
-   Експортує вміст директорії SVN
    

# svnexport

(PECL svn >= 0.3.0)

svnexport — Експортує вміст директорії SVN

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

При **`true`** з робочої копії будуть також експортовані ненаправлені в репозиторій файли.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **svnexport()****

```php
<?php
$working_dir     = '../';
$new_working_dir = '/home/user/devel/foo/trunk';

svn_export($working_dir, $new_working_dir);
?>
```

### Дивіться також

-   [svn\_import()](function.svn-import.html) - Імпорт шляху без версії до репозиторії