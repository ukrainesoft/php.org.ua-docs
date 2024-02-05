---
navigation:
  - function.svn-fs-contents-changed.md: « svn\_fs\_contents\_changed
  - function.svn-fs-delete.md: svn\_fs\_delete »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svn\_fs\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# svn\_fs\_copy

(PECL svn >= 0.2.0)

svn\_fs\_copy — Копіює файл або директорію

### Опис

```methodsynopsis
svn_fs_copy(    resource $from_root,    string $from_path,    resource $to_root,    string $to_path): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Копіює файл або директорію.

### Список параметрів

`from_root`

`from_path`

`to_root`

`to_path`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
