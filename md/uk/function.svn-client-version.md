---
navigation:
  - function.svn-cleanup.md: « svn\_cleanup
  - function.svn-commit.md: svn\_commit »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_client\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_client\_version

(PECL svn >= 0.1.0)

svn\_client\_version — Повертає версію клієнтських бібліотек SVN

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
echo svn_client_version();
?>
```

Висновок наведеного прикладу буде схожим на:

```
1.3.1
```

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
