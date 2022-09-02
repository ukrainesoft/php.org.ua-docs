---
navigation:
  - function.svn-auth-set-parameter.md: « svnauthsetparameter
  - function.svn-cat.md: svncat »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svnblame
---
# svnblame

(PECL svn >= 0.3.0)

svnblame — Построчно виводить автора та редакцію для файлу

### Опис

```methodsynopsis
svn_blame(string $repository_url, int $revision_no = SVN_REVISION_HEAD): array
```

Рядково виводить автора та редакцію для файлу з репозиторію.

### Список параметрів

`repository_url`

URL-репозиторія.

`revision_no`

Номер ревізії.

### Значення, що повертаються

array Порядковий масив з наступною інформацією: номер ревізії, номер рядка, рядок коду, автор та дата.

### Приклади

**Приклад #1 Приклад використання функції **svnblame()****

```php
<?php
$svnurl = 'http://svn.example.org/svnroot/foo/trunk/index.php';

print_r( svn_blame($svnurl) );

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] = Array
          (
           [rev] = 1
           [line_no] = 1
           [line] = Hello World
           [author] = joesmith
           [date] = 2007-07-02T05:51:26.628396Z
          )
    [1] = Array
          ...
```

### Дивіться також

-   [svndiff()](function.svn-diff.md) - Рекурсивно показує різницю двох файлів
-   **svnlogs()**
-   [svnstatus()](function.svn-status.md) - Повертає SVN-статус файлів та директорій робочої копії
