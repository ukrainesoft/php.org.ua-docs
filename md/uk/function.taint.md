---
navigation:
  - function.is-tainted.html: « istainted
  - function.untaint.html: untaint »
  - index.html: PHP Manual
  - ref.taint.html: Функции Taint
title: taint
---
# taint

(PECL taint >=0.1.0)

taint — зіпсувати рядок

### Опис

```methodsynopsis
taint(string &$string, string ...$strings): bool
```

Робить рядок зіпсований рядок. Використовується з метою налагодження.

### Список параметрів

`string`

`strings`

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо перетворення рядка виконано. Завжди повертає \*\*`true`\*\*якщо модуль taint не включений.
