---
navigation:
  - function.svn-cleanup.html: « svncleanup
  - function.svn-commit.html: svncommit »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svnclientversion
---
# svnclientversion

(PECL svn> = 0.1.0)

svnclientversion — Повертає версію клієнтських бібліотек SVN

### Опис

```methodsynopsis
svn_client_version(): string
```

Повертає версію клієнтських бібліотек SVN

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Номер версії зазвичай у форматі x.y.z.

### Приклади

**Приклад #1 Простий приклад**

```php
<?php
echo svn_client_version();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1.3.1
```

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
