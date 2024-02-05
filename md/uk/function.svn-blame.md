---
navigation:
  - function.svn-auth-set-parameter.md: « svn\_auth\_set\_parameter
  - function.svn-cat.md: svn\_cat »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_blame
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_blame

(PECL svn >= 0.3.0)

svn\_blame — Построчно виводить автора та редакцію для файлу

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

**Приклад #1 Приклад использования функции**svn\_blame()\*\*\*\*

```php
<?php
$svnurl = 'http://svn.example.org/svnroot/foo/trunk/index.php';

print_r( svn_blame($svnurl) );

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [svn\_diff()](function.svn-diff.md) \- Рекурсивно показує різницю двох файлів
-   **svn\_logs()**
-   [svn\_status()](function.svn-status.md) \- Повертає SVN-статус файлів та директорій робочої копії
