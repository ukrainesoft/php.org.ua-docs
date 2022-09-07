---
navigation:
  - function.svn-fs-check-path.md: « svnфсcheckpath
  - function.svn-fs-copy.md: svnфсcopy »
  - index.md: PHP Manual
  - ref.svn.md: Функції SVN
title: svnфсcontentschanged
---
# svnфсcontentschanged

(PECL svn >= 0.2.0)

svnфсcontentschanged - Повертає **`true`**, якщо вміст відрізняється або **`false`** в іншому випадку

### Опис

```methodsynopsis
svn_fs_contents_changed(    resource $root1,    string $path1,    resource $root2,    string $path2): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає **`true`**, якщо вміст відрізняється або **`false`** в іншому випадку.

### Примітки

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.
