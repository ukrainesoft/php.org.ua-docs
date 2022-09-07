---
navigation:
  - function.svn-fs-contents-changed.md: « svnфсcontentschanged
  - function.svn-fs-delete.md: svnфсdelete »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svnфсcopy
---
# svnфсcopy

(PECL svn >= 0.2.0)

svnфсcopy — Копіює файл або директорію

### Опис

```methodsynopsis
svn_fs_copy(    resource $from_root,    string $from_path,    resource $to_root,    string $to_path): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Копіює файл або директорію.

### Список параметрів

`from_root`

`from_path`

`to_root`

`to_path`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
